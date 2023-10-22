#!/usr/bin/python3
import sys

def factorize(n):
    factors = []
    for i in range(2, n // 2 + 1):
        if n % i == 0:
            factors.append((i, n // i))
    return factors

def main(filename):
    try:
        with open(filename, 'r') as file:
            for line in file:
                n = int(line)
                factorizations = factorize(n)
                for factorization in factorizations:
                    p, q = factorization
                    print(f"{n}={p}*{q}")
    except FileNotFoundError:
        print(f"File not found: {filename}")
    except ValueError:
        print("Invalid input. Please make sure the file contains valid natural numbers.")

if __name__ == "__main__":
    if len(sys.argv) != 2:
        print("Usage: factors <file>")
    else:
        filename = sys.argv[1]
        main(filename)

