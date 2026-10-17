# 🔥 GOLDFIRE V3 by Somenath (13)

**Rule: Q = N - P** Python Code to test:
for p in primes:
  q = n - p
  if is_prime(q): print(p,q)

**Founder:** Somenath, 13, BANKURA, West Bengal, India
**Project Type:** Educational Research on Number Theory

### What is Goldfire?
My method to explore Goldbach's Conjecture: Every even N > 2 can be written as N = P + Q where P, Q are primes.

This is my own way to find and count prime pairs for any even number.

### Example: N = 30
30 = 7+23, 11+19, 13+17
G(30) = 3 pairs (Goldbach partition count)

### Formula
Q = N - P
If Q is prime, we found a valid pair.
We loop P over primes < N and count.

### Python Logic (My Method)
```python
def goldfire_pairs(n):
    pairs = []
    for p in range(2, n):
        if is_prime(p):
            q = n - p
            if is_prime(q):
                pairs.append((p,q))
    return pairs
