# **III. Properties of Secure Hash Functions**

To be effective in cryptographic applications, hash functions must possess specific properties that make them resistant to attacks. These properties are essential for maintaining data integrity and ensuring that hash functions can be trusted in secure environments.

## **A. Pre-image Resistance**

- **Definition**: Given a hash output (H), it should be computationally infeasible to determine the original input (M) that produced H.
- **Importance**: Pre-image resistance ensures that an attacker cannot retrieve the original data simply by knowing the hash, making it useful for storing sensitive information like passwords.

## **B. Second Pre-image Resistance**

- **Definition**: Given an input (M1) and its hash output (H1), it should be computationally infeasible to find a different input (M2) such that the hash of M2 also equals H1.
- **Importance**: Second pre-image resistance prevents an attacker from creating a fake message with the same hash as the original, helping to maintain data integrity.

## **C. Collision Resistance**

- **Definition**: It should be computationally infeasible to find two distinct inputs (M1 and M2) that produce the same hash output (H).
- **Importance**: Collision resistance is crucial for ensuring the uniqueness of each hash. If two different inputs produce the same hash, it can lead to security vulnerabilities, especially in applications like digital signatures, where a collision could allow forgery.

## **D. Avalanche Effect**

- **Definition**: A minor change in the input should result in a significantly different hash output. Even a single bit change in the input should alter at least half of the output bits in an unpredictable way.
- **Importance**: The avalanche effect is vital for making patterns or relationships between inputs and their hashes untraceable, thereby enhancing security and making attacks like differential cryptanalysis more difficult.
