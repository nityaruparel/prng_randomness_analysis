# Nothing is Random

*Exploring why “random-looking” isn’t enough*

---

## Overview

We tend to treat randomness as a solved problem.

Call `random()` and move on.

But once you look a bit closer, things get less obvious. A sequence can look completely random, pass standard tests, and still be predictable.

This project started from that idea and split into two parts:

* Part 1 looks at whether “random-looking” systems can still be predicted
* Part 2 explores whether machine learning can detect patterns that statistical tests miss

---

## The idea in one line

Different approaches to randomness answer different questions:

* Statistical tests → does this look random?
* Machine learning → is there any pattern here?
* Security → can someone predict what comes next?

This project shows how those answers don’t always agree.

---

## What’s included

### Part 1 — The illusion of randomness

* Basic PRNG behavior
* A simple seed-based attack
* Demonstration that:

  * sequences can look random
  * pass tests
  * and still be predictable

---

### Part 2 — Entropy fingerprinting

* Comparison of:

  * LCG
  * LFSR
  * Python `random` (Mersenne Twister)
  * `os.urandom`

* NIST-style statistical tests

* Bit-level feature extraction (per-bit autocorrelation, etc.)

* Random Forest model to classify generators

* t-SNE visualization to understand structure

---

## Key observations

* Some generators fail obvious tests (like LFSR)
* Some pass everything but still have structure (like LCG)
* Machine learning can pick up those hidden patterns
* Strong generators don’t leave anything detectable in their output

A system can pass tests, look random, and still be predictable.

---

## Blog posts

Part 1:
[[Nothing is Random Part1](https://medium.com/@ruparelnitya/nothing-is-random-part-1-c5a4167c9fcd)]

Part 2:
[[Nothing is Random Part2](https://medium.com/@ruparelnitya/nothing-is-random-part-2-86bcdd9799c8)]

---

## Why this matters

Randomness is often judged by how it looks.

But for real systems, what matters is whether it can be predicted.

That difference shows up in subtle ways — and it’s easy to miss if you only rely on standard tests.

---

## Final note

This isn’t about building a better randomness test.

It’s about understanding that:
what looks random, what behaves random, and what is secure
are not always the same thing.

