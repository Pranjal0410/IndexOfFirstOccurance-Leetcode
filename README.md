Find the Index of the First Occurrence in a String
Problem Statement
Given a string and a target substring, your task is to find the index of the first occurrence of the target substring within the given string. If the substring is not found, return -1.

Function Signature:

python
Copy code
def find_first_occurrence(main_string, target_substring):
    # Your code here
Input
main_string (1 <= len(main_string) <= 10^5): A string in which you need to find the target substring.
target_substring (1 <= len(target_substring) <= 100): The substring to search for in the main_string.
Output
Return the index of the first occurrence of the target_substring in the main_string. If it is not found, return -1.
Examples
python
Copy code
find_first_occurrence("hello world", "lo")  # Output: 3
find_first_occurrence("abcde", "z")          # Output: -1
find_first_occurrence("programming", "gram") # Output: 3
Solution
To solve this problem, you can use a simple iteration through the main_string, checking if the current substring of the same length as the target_substring matches it. If a match is found, return the current index. If you reach the end of the string without finding a match, return -1.

Here's a Python function that accomplishes this:

python
Copy code
def find_first_occurrence(main_string, target_substring):
    for i in range(len(main_string) - len(target_substring) + 1):
        if main_string[i:i + len(target_substring)] == target_substring:
            return i
    return -1
Complexity Analysis
The time complexity of this solution is O(N * M), where N is the length of the main_string, and M is the length of the target_substring. In the worst case, you may need to compare every possible substring of the main_string, which makes it a relatively straightforward solution.

