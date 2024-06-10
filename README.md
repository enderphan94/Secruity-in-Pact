# Secruity-in-Pact
Aims to create a security concern and checklist for Pact

# Checklist

OWASP + PACT

| **Category**             | **Checklist Item**                                                                 | **Description**                                                                                     |
|--------------------------|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| **Input Validation**     | Validate all inputs                                                                | Ensure all user inputs are validated to prevent injection attacks.                                   |
|                          | Use strict data types                                                              | Enforce strict data types for all inputs.                                                            |
|                          | Implement whitelist validation                                                     | Only accept known good inputs, reject all others.                                                    |
| **Output Encoding**      | Encode outputs properly                                                            | Prevent data leakage by encoding outputs correctly.                                                  |
| **Authentication and Password Management** | Ensure proper authentication mechanisms are in place                             | Verify that only authorized users can access the contract functions.                                 |
|                          | Implement multi-factor authentication                                             | Use additional authentication methods to secure access.                                              |
|                          | Store passwords securely                                                          | Use strong hashing algorithms to store passwords.                                                    |
|                          | Implement account lockout mechanisms                                              | Prevent brute force attacks by locking accounts after several failed login attempts.                 |
| **Access Control**       | Verify role-based access control (RBAC)                                            | Ensure roles are properly defined and enforced within the contract.                                  |
|                          | Check for least privilege principle                                                | Ensure users and roles have the minimum necessary permissions.                                        |
|                          | Implement access control lists (ACLs)                                              | Use ACLs to control which addresses can interact with the contract.                                  |
| **Cryptographic Practices** | Encrypt sensitive data                                                             | Use strong encryption to protect sensitive data both at rest and in transit.                         |
|                          | Implement data integrity checks                                                    | Ensure data integrity through checksums or hashes.                                                   |
|                          | Avoid using weak cryptographic algorithms                                          | Use strong and current cryptographic algorithms.                                                     |
| **Error Handling and Logging** | Implement comprehensive error handling                                             | Ensure errors are handled gracefully without exposing sensitive information.                         |
|                          | Implement logging for critical operations                                          | Log critical operations and ensure logs are securely stored.                                         |
|                          | Monitor for abnormal activities                                                    | Regularly monitor logs for unusual or malicious activities.                                          |
| **Data Protection**      | Protect sensitive data                                                             | Ensure sensitive data is encrypted and access is restricted.                                         |
|                          | Implement data masking                                                             | Mask sensitive data when displaying it to unauthorized users.                                        |
| **Communication Security** | Use secure communication channels                                                | Ensure data is transmitted over secure channels (e.g., HTTPS).                                       |
|                          | Implement mutual authentication                                                    | Verify both ends of the communication channel.                                                       |
| **System Configuration** | Ensure secure default settings                                                     | Ensure systems are securely configured out of the box.                                               |
|                          | Regularly update and patch systems                                                 | Keep systems up to date with the latest security patches.                                            |
| **Smart Contract Specific** | Ensure deterministic contract logic                                            | Verify that contract logic is deterministic and not dependent on external factors.                   |
|                          | Conduct formal verification                                                        | Use formal methods to prove the correctness of the contract logic.                                   |
|                          | Limit use of external contracts                                                    | Minimize dependencies on external contracts to reduce attack surface.                                |
|                          | Perform regular audits                                                             | Conduct regular security audits of the contract code.                                                |
|                          | Use Pact's built-in guards                                                         | Leverage Pact's native security features such as keyset guards and capabilities.                     |
|                          | Test for replay attacks                                                            | Ensure that the contract is resistant to replay attacks.                                             |
|                          | Avoid using hardcoded secrets                                                      | Ensure no hardcoded secrets or sensitive information are present in the contract code.               |
| **General Security Practices** | Conduct threat modeling and risk assessments                                    | Regularly evaluate potential threats and risks to the contract.                                       |
|                          | Maintain a secure development lifecycle                                            | Follow security best practices throughout the development lifecycle.                                 |
|                          | Ensure proper documentation                                                        | Maintain thorough documentation of the contract's design and security features.                      |
|                          | Train developers on secure coding practices                                        | Ensure developers are trained on the latest secure coding practices.                                 |
