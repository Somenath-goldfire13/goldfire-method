# 🔥 GOLDFIRE V3 - The Ultimate Method for Goldbach's Conjecture
### Rule: Q = N - P
> Founder & Creator: **Somenath Das, 13 Years Old, BANKURA, West Bengal, India**

### 🚀 What is GOLDFIRE?
Goldfire is my original educational method to explore and visualize Goldbach's Conjecture.
**Goldbach's Conjecture:** Every even number N > 2 can be expressed as the sum of two prime numbers, N = P + Q.

My method provides a simple, fast, and systematic way to find all prime pairs for any even number.

### 🧠 The Core Formula
**Q = N - P**
Where:
- **N** = Any Even Number (e.g., 30, 100, 1000)
- **P** = A prime number less than N
- **Q** = N - P. If Q is also prime, we have found a Goldbach partition.

### 💡 My Methodology
1.  Take an even number N.
2.  Loop through all primes P < N.
3.  Calculate Q = N - P.
4.  Check if Q is prime using primality test.
5.  If yes, (P, Q) is a valid pair. Count it.
6.  G(N) = Total number of such pairs for N.

### 📊 Example: N = 30 (Detailed)
N = 30
- P=7, Q=23 (Prime) -> Valid
- P=11, Q=19 (Prime) -> Valid
- P=13, Q=17 (Prime) -> Valid
**Result: G(30) = 3 pairs.**

### 🐍 Python Code - My Original Logic
```python
def is_prime(num):
    if num < 2: return False
    for i in range(2, int(num**0.5)+1):
        if num % i == 0:
            return False
    return True

def goldfire_pairs(n):
    pairs = []
    for p in range(2, n):
        if is_prime(p):
            q = n - p
            if is_prime(q):
                pairs.append((p, q))
    return pairs

print(goldfire_pairs(30))
