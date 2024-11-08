# **VII. How Digital Signatures Ensure Data Integrity and Authenticity**

Digital signatures use hash functions and asymmetric encryption to verify that data has not been tampered with and that it originates from a legitimate source. This process ensures both **data integrity** and **authenticity**.

## **A. Signing Process**

1. **Hashing the Data**:
   - The sender starts by generating a hash of the original message or document.
   - This hash serves as a unique fingerprint for the data. Any alteration, even a minor one, would result in a different hash.

2. **Creating the Digital Signature**:
   - The sender then encrypts this hash using their private key, producing the digital signature.
   - Since the private key is only known to the sender, this signature assures the recipient of the sender’s identity.

3. **Transmitting Data and Signature**:
   - The original data and the digital signature are both sent to the recipient.

## **B. Verification Process**

1. **Hashing the Received Data**:
   - The recipient hashes the received data to generate a new hash. This step ensures that any changes to the data, intentional or accidental, are detected.

2. **Decrypting the Signature**:
   - The recipient uses the sender’s public key to decrypt the digital signature, which reveals the hash originally created by the sender.

3. **Hash Comparison**:
   - The recipient compares the decrypted hash with the newly generated hash.
   - If the hashes match, the data is verified as authentic and unaltered.
   - If they do not match, it indicates either that the data was tampered with or that the signature is not genuine.

## **C. Role of Hash Functions in Digital Signatures**

Hash functions are essential in digital signatures as they provide a fixed-size, unique representation of the data. The properties of hash functions, like pre-image resistance and collision resistance, ensure that:

- **Tampering Detection**: Any modification to the data invalidates the signature.
- **Efficiency**: Hashing the data before encryption is more efficient than encrypting the entire document, especially for large data files.
