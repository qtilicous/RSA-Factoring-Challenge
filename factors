#!/usr/bin/python3

import sys


def factorize(n):
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return i, n // i
    return n, 1


if len(sys.argv) != 2:
    print("Usage: factors <file>")
    sys.exit(1)

input_file = sys.argv[1]

try:
    with open(input_file, 'r') as file:
        for line in file:
            n = int(line.strip())
            p, q = factorize(n)
            print(f"{n}={p}*{q}")

except FileNotFoundError:
    print(f"Error: File '{input_file}' not found.")
    sys.exit(1)
except ValueError:
    print("Error: Invalid input. All lines should be numbers greater than 1.")
    sys.exit(1)
