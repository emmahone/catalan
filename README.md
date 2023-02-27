# catalan

Here's a simple Python script to calculate the Catalan numbers using a recursive function:
~~~
def catalan(n):
    if n <= 1:
        return 1

    res = 0
    for i in range(n):
        res += catalan(i) * catalan(n-i-1)

    return res

# Calculate and print the first 10 Catalan numbers
for n in range(10):
    print(catalan(n))
~~~
This script defines a function catalan that takes an integer n as input and returns the n-th Catalan number. The function uses a recursive formula to compute the Catalan number, which is defined as follows:
~~~
Catalan(n) = (2n)! / (n! * (n+1)!)
~~~
The script then calculates and prints the first 10 Catalan numbers using a for loop.

You can run this script in a Python environment or in a command line by saving the code in a file with a .py extension and running it using python filename.py command.

Here's a test case for the catalan function in the script above:
~~~
def test_catalan():
    assert catalan(0) == 1
    assert catalan(1) == 1
    assert catalan(2) == 2
    assert catalan(3) == 5
    assert catalan(4) == 14
    assert catalan(5) == 42
    assert catalan(6) == 132
    assert catalan(7) == 429
    assert catalan(8) == 1430
    assert catalan(9) == 4862
~~~

This test function defines multiple assertions that test the catalan function for different input values. Each assertion checks whether the output of the catalan function for a specific input value is equal to the expected value. The expected values are taken from a known sequence of Catalan numbers.

You can run this test function in a Python environment or in a command line by calling test_catalan() function. If all assertions pass, the function will execute without any output. If one or more assertions fail, an AssertionError will be raised indicating which assertion(s) failed and what was the actual output.
