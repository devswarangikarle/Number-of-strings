# Number-of-strings
Given a length n, count the number of strings of length n that can be made using a,  b and c.

def count_strings_of_length_n(n):
    if n == 1:
        return 3  # 'a', 'b', 'c'
    if n == 2:
        return 3 * 3  # 'aa', 'ab', 'ac', 'ba', 'bb', 'bc', 'ca', 'cb', 'cc'

    return 3 * count_strings_of_length_n(n - 1)

n = int(input().strip())

result = count_strings_of_length_n(n)
print(result)
