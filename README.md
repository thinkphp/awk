# awk
The name "AWK" comes from the initials of its creators: Alfred Aho, Peter Weinberger, and Brian Kernighan


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
