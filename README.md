# awk
The name "AWK" comes from the initials of its creators: Alfred Aho, Peter Weinberger, and Brian Kernighan


#### How to Install

AWK is typically included by default in most Unix-like operating systems, including Ubuntu. However, if for any reason it's not installed on your system, you can install it using the package manager. Here's how you can install AWK on Ubuntu:

Open a terminal and type the following command:

```
sudo apt-get update
sudo apt-get install gawk
gawk --version
```

### Example0

```
# Ackermann function in AWK
function ackermann(m, n) {
    if (m == 0) {
        return n + 1
    } else if (m > 0 && n == 0) {
        return ackermann(m - 1, 1)
    } else if (m > 0 && n > 0) {
        return ackermann(m - 1, ackermann(m, n - 1))
    }
}

# Example: Calculate A(2, 3)
BEGIN {
    result = ackermann(2, 3)
    print "A(2, 3) =", result
}

```

```
awk -f ackermann.awk

```

### Example1

Now, suppose you want to extract and print the names of people who are older than 30. You can use AWK for this task. Here's a simple AWK command:

```
Name, Age, City
Alice, 28, New York
Bob, 35, San Francisco
Charlie, 22, Los Angeles
David, 40, Chicago

```

```
awk -F', ' '$2 > 30 {print $1}' sample.txt

```

### Example2

```
# Calculate the factorial of a number using recursion
function factorial(n) {
    if (n <= 1) {
        return 1
    } else {
        return n * factorial(n - 1)
    }
}

# Example: Calculate the factorial of 5
BEGIN {
    number = 5
    result = factorial(number)
    print "The factorial of " number " is: " result
}

```

```
awk -f factorial.awk

```
