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
