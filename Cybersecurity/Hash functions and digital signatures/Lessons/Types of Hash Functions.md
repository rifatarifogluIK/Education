# **II. Types of Hash Functions**

Hash functions come in various forms, each suited to different purposes. While **cryptographic hash functions** are designed for security-critical applications, **non-cryptographic hash functions** are generally used for tasks like checksums or error-checking.

## **A. Cryptographic Hash Functions**

These hash functions are specifically designed to be secure and resistant to various types of attacks. They are widely used in data integrity verification, digital signatures, and other cryptographic applications.

1. **MD5 (Message Digest Algorithm 5)**:
   - Once popular for data integrity checks, MD5 produces a 128-bit hash.
   - It’s now considered insecure due to vulnerability to collision attacks, where two different inputs produce the same hash. MD5 is still found in legacy systems but is no longer recommended for secure applications.

2. **SHA (Secure Hash Algorithm) Family**:
   - Developed by the National Security Agency (NSA), the SHA family includes several widely used ryptographic hash functions:
   - **SHA-1**: Produces a 160-bit hash and was commonly used in SSL certificates and digital signatures. However, SHA-1 is now deprecated due to vulnerabilities to collision attacks.
   - **SHA-2**: This family includes SHA-224, SHA-256, SHA-384, and SHA-512, named according to their output size in bits. SHA-2 is considered secure and is widely used in applications requiring strong security, such as SSL/TLS, Bitcoin, and file integrity verification.
   - **SHA-3**: Developed as an alternative to SHA-2, SHA-3 uses a different internal structure called a **sponge construction**. It includes versions like SHA3-256 and SHA3-512, offering similar security to SHA-2 with additional resistance to specific types of cryptographic attacks.

3. **BLAKE and BLAKE2**:
   - BLAKE is another family of cryptographic hash functions, created as an alternative to the SHA family.
   - **BLAKE2** is a high-speed, cryptographically secure hash function designed as an improvement over MD5 and SHA-2 in terms of speed and security.
   - BLAKE3, an enhancement of BLAKE2, offers even greater performance and is highly scalable, suitable for modern multi-core processors.

## **B. Non-Cryptographic Hash Functions**

Non-cryptographic hash functions are often used for data verification, checksums, or other applications where high security isn’t required. They are generally faster but lack the robust security features of cryptographic hashes.

1. **CRC (Cyclic Redundancy Check)**:
   - Commonly used for error-checking in data transmission. CRC is a simple hash function that helps detect accidental changes in data.
   - Widely used in network communications, storage devices, and file formats but is not suitable for security-critical applications.

2. **Adler-32**:
   - A non-cryptographic hash function that generates a 32-bit hash. It’s faster than CRC and used in applications where speed is more important than security.
   - Often found in compression algorithms like zlib but lacks robustness for cryptographic purposes.

3. **Fowler-Noll-Vo (FNV)**:
   - FNV is a fast, simple, non-cryptographic hash function that generates hashes efficiently for data structures, like hash tables.
   - Primarily used in applications requiring quick data lookups, such as hashing in programming languages.
