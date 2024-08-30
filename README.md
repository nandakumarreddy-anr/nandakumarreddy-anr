Given an array arr of positive integers sorted in a strictly increasing order, and an integer k.
Return the kth positive integer that is missing from this array.
Example 1:
Input: arr = [2,3,4,7,11], k = 5
Output: 9
arr = [2, 3, 4, 7, 11]
k = 5

missing = 0
expected = 1
for num in arr:
    while expected < num:
        missing += 1
        if missing == k:
            print(expected)
            break
        expected += 1
    expected += 1
else:
    print(expected + k - missing - 1)

