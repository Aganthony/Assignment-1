# Amarachi Anthony
# CIDM 6330 
# Assignment 1 Kata - Roman Numerals

## Transforming Roman Numerals value
Creating a variable to store input value
```python
ver = input()
def RomanNumeralToNumber(ver):
    # Associate each Roman numeral character with its respective numeric value.
    d = {"M": 1000, "D": 500, "L": 50, "C": 100, "X": 10, "V": 5, "I": 1}
    # Setting the Initial value of the numberic variable to zero 
    int = 0
    # Convert input to uppercase to handle both lower and upper case input
    ver = ver.upper()
    # Iterate through the dictionary's Roman numeral characters using a for loop based on the stored variable value
    for num in range(len(ver)):
        # Applying an if statement to verify the value at the first index in the variable
        # If the value at the first index of the condition is smaller than the corresponding dictionary value
        # subtract the  from the variable
        if num + 1 != len(ver) and d[ver[num]] < d[ver[num + 1]]:
            int = int - d[ver[num]]
        # else add the value to the variable
        else:
            int = int + d[ver[num]]
    # return the result of the variable
    return int
if all(char in "IVXLCMD" for char in ver.upper()):
    print("Your Answer is number:", RomanNumeralToNumber(ver))
else:
    print("You Have Entered an Invalid Roman Numeral, Please Try Again")

### Video - Converting Roman Numeral to Integer Number
[Video Experience on converting Roman Numeral to integer]
(https://drive.google.com/file/d/1I5WK1s6qt5Bbv508_GVF8K2WYrhxKAJs/view?usp=drive_link)
