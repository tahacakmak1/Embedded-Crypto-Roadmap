# Guiding principle

Don't think of your studies as **three separate tracks**:

* C++
* DSA
* Cryptography

Instead, think of them as one integrated skill:

> **Writing high-quality cryptographic software in modern C++ for embedded systems.**

---

## Weekly Schedule

| Day       | Time | Focus                                     | Book                                   |
| --------- | ---- | ----------------------------------------- | ---------------------------------------|
| Monday    | 2 h  | Cryptography (Theory)                     | **Serious Cryptography**               |
| Tuesday   | 2 h  | DSA                                       | **Wengrow** + **Karumanchi**           |
| Wednesday | 2 h  | Cryptography (Internals)                  | **Understanding Cryptography**         |
| Thursday  | 2 h  | DSA                                       | **Wengrow** + **Karumanchi**           |
| Friday    | 2 h  | Cryptography (Implementation & Standards) | **Real World Cryptography**            |
| Saturday  | 4 h  | C++ Course                                | 1 Lecture                              |
| Sunday    | 4 h  | C++ exercises + applying concepts         | **Effective Modern C++** (1 item/week) |

---

## Monday - Cryptography (Theory)

**Primary book:** ***Serious Cryptography***

Goal: ***Understand **what** an algorithm does and **why** it exists.***

Examples:

* AES
* SHA-256
* HMAC
* HKDF
* ECDSA
* Certificates

Ask questions like:

* Why is AES-GCM preferred over AES-CBC?
* Why is nonce reuse catastrophic?
* Why is HKDF needed?

Take notes in your own words.

---

## Tuesday - DSA

Use both books together.

### 20-30 min

* Read ***Wengrow***
* Understand the intuition.

### 30-40 min

* Read ***Karumanchi***
* See how it's implemented.

### 50-60 min

* Close both books.
* Implement everything yourself.
* No copying.

---

## Wednesday - Cryptography (Internals)

**Primary book:** ***Understanding Cryptography***

Stay on the same topic as Monday.

Example:

Monday

AES

↓

Wednesday

Learn

* finite fields
* S-box
* MixColumns
* Key Expansion

Now you understand how AES actually works.

This is the difference between *using* cryptography and *implementing* cryptography.

---

## Thursday - DSA

Continue implementing.

Then

* write tests
* benchmark
* improve design
* solve a couple of problems

Since you now have only **two DSA days**, I'd spend **two weeks per topic** instead of rushing
through them.

Quality > quantity.

---

## Friday - Cryptography (Implementation)

Rotate between:

* **Real-World Cryptography**
* NIST standards
* RFCs
* Reading mbedTLS/BoringSSL/OpenSSL
* Small implementations

Example progression:

Week 1

Implement HKDF.

Week 2

Read RFC 5869.

Week 3

Compare with mbedTLS.

Week 4

Write tests and benchmarks.

This is probably the highest-value session because it connects theory with production code.

---

## Saturday - C++ Course

Watch approximately **one lecture** (3.5 hours).

Take notes.

Don't rush.

Your course is a long-term investment.

---

## Sunday - Apply the C++

This is the most important day.

Don't immediately watch another lecture.

Instead:

* Complete exercises from Saturday.
* Refactor your DSA implementations.
* Improve your crypto code.

Examples:

Lecture:

Templates

↓

Convert

```cpp
Stack<int>
```

into

```cpp
template<typename T>
class Stack
```

Lecture:

Move semantics

↓

Improve

```cpp
Vector
```

Lecture:

Smart pointers

↓

Rewrite ownership.

Lecture:

`constexpr`

↓

Improve compile-time utilities.

This is where the C++ course becomes practical skill.

---

## Where each book fits

| Book                           | Purpose                    | When                 |
| ------------------------------ | -------------------------- | -------------------- |
| **Serious Cryptography**       | Practical crypto concepts  | Monday               |
| **Understanding Cryptography** | Crypto internals           | Wednesday            |
| **Real-World Cryptography**    | Protocols & systems        | Friday               |
| **Wengrow**                    | Build intuition            | Tuesday              |
| **Karumanchi**                 | Learn implementation       | Tuesday & Thursday   |
| **Effective Modern C++**       | Modern C++ best practices  | Sunday (1 item/week) |
| **Pragmatic Programmer**       | Engineering habits         | Casual reading       |
| **Hacker's Delight**           | Bit manipulation reference | As needed            |
| **C++ Concurrency in Action**  | Advanced C++               | After the C++ course |

---

## Effective Modern C++

Treat it as your "slow book."

Read **one Item per week**.

Then immediately apply it.

Example:

Read an Item on move semantics.

↓

Improve your `Vector`.

Read an Item on `auto`.

↓

Review your codebase.

Read an Item on smart pointers.

↓

Improve ownership.

Never binge-read this book.

---

## Pragmatic Programmer

Don't schedule it.

Read

10-20 pages before bed.

Think:

> "Can I apply this idea at work tomorrow?"

---

## Hacker's Delight

Don't study it sequentially.

Instead, whenever you encounter something like:

```cpp
x &= x - 1;
```

or

```cpp
std::rotl(x, n)
```

or a branchless comparison,

look up the relevant chapter.

This is exactly how professionals use it.

---

## C++ Concurrency in Action

Wait until your course has covered:

* threads
* atomics
* memory model

Then read one chapter every couple of weeks.

There's no benefit in reading it too early.

---

## One integrated repository

```text
embedded-crypto-roadmap/
├── cpp-foundations/
│   ├── graph/
│   ├── hashmap/
│   ├── heap/
│   ├── linked_list/
│   └── vector/
├── crypto/
│   ├── asymmetric/
│   │   ├── ecc/
│   │   │   ├── ed25519/
│   │   │   └── secp256r1/
│   ├── boot/
│   │   └── secure_boot/
│   ├── cetificates/
│   │   └── x509/
│   ├── hash/
│   │   ├── blake2/
│   │   ├── sha256/
│   │   └── sha3/
│   ├── kdf/
│   │   ├── hkdf/
│   │   └── pbkdf2/
│   ├── mac/
│   │   ├── cmac/
│   │   └── hmac/
│   ├── protocols/
│   │   └── tls_handshake_demo/
│   ├── rng/
│   │   └── ctr_drbg/
│   ├── signature/
│   │   ├── ecdsa/
│   │   └── ed25519/
│   └── symmetric/
│       └── aes/
│           ├── cbc/
│           ├── ctr/
│           ├── ecb/
│           └── gcm/
├── playground/
├── benchmarks/
└── tests/
```

As your C++ skills improve, revisit older implementations instead of leaving them behind. That
demonstrates growth and mirrors how production software evolves.

---

## Long-term progression

### Months 1-3

#### DSA focus

* Vector
* Linked List
* Stack
* Queue
* Hash Table
* Heap

#### Crypto focus

* Hashes
* HMAC
* AES
* Modes of operation

---

### Months 4-6

#### DSA

* Trees
* Graphs
* Sorting
* Dynamic Programming (fundamentals)

#### Crypto

* ECC
* ECDSA
* HKDF
* Random number generation
* Certificates

---

### Months 7-12

Shift the emphasis toward embedded cryptography.

Build:

* SHA-256 implementation
* HMAC
* HKDF
* DER/ASN.1 parser
* X.509 parser
* Secure Boot demonstration
* Firmware signature verification

By this stage, DSA should become maintenance rather than your primary focus.

---

## Why I think this is the strongest plan

Your objective isn't to become a generalist software engineer or a competitive programmer. It's to
become an **Embedded Cryptography Engineer**.

This schedule reflects that:

* **Cryptography** becomes your deepest area of expertise.
* **DSA** gives you the implementation confidence needed for interviews.
* **Modern C++** raises the quality of everything you write.
* **Engineering books** improve how you design, maintain, and reason about software.

The result is that, by the time you're interviewing, you won't just be able to explain cryptographic
concepts—you'll be able to**implement them cleanly, test them rigorously, and express them in modern C++**,
which is exactly the combination many embedded security teams are looking for.
