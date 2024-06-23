# Secruity-in-Pact
Aims to create a security concern and checklist for Pact

# Checklist

OWASP + PACT

| #  | Checklist Item                              | Description                                                                 |
|----|---------------------------------------------|-----------------------------------------------------------------------------|
| 1  | Validate all inputs                         | Ensure all user inputs are validated to prevent injection attacks.          |
| 2  | Use strict data types                       | Enforce strict data types for all inputs.                                   |
| 3  | Implement whitelist validation              | Only accept known good inputs, reject all others.                           |
| 4  | Ensure proper authentication mechanisms     | Verify that only authorized users can access the contract functions.        |
| 5  | Implement multi-factor authentication       | Use additional authentication methods to secure access.                     |
| 6  | Verify role-based access control (RBAC)     | Ensure roles are properly defined and enforced within the contract.         |
| 7  | Check for least privilege principle         | Ensure users and roles have the minimum necessary permissions.              |
| 8  | Implement access control lists (ACLs)       | Use ACLs to control which addresses can interact with the contract.         |
| 9  | Implement comprehensive error handling      | Ensure errors are handled gracefully without exposing sensitive information.|
| 10 | Ensure deterministic contract logic         | Verify that contract logic is deterministic and not dependent on external factors.|
| 11 | Conduct formal verification                 | Use formal methods to prove the correctness of the contract logic.          |
| 12 | Limit use of external contracts             | Minimize dependencies on external contracts to reduce attack surface.       |
| 13 | Use Pact's built-in guards                  | Leverage Pact's native security features such as keyset guards and capabilities.|
| 14 | Test for replay attacks                     | Ensure that the contract is resistant to replay attacks.                    |
| 15 | Avoid using hardcoded secrets               | Ensure no hardcoded secrets or sensitive information are within the contract code.|
| 16 | Cross-Function Reentrancy                   | Ensure no recursive call.                                                   |


# Attacks

* Re-entrancy attack: [https://hackernoon.com/hack-solidity-reentrancy-attack](https://www.certik.com/resources/blog/1eFmMTGVicfAMiPka3vaTY-cross-function-reentrancy-attacks-in-kadena-smart-contracts)


