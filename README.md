# Security-in-Pact
Aims to create a security concern and checklist for Pact

# Gen key-pair account

https://github.com/kadena-community/secure-keygen

```dd if=/dev/urandom bs=32 count=1 | ./keygen keys```

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

# Tools

* Use chainweaver to see the overall functions of a contract: http://chainweaver.kadena.network
* Use Cspell to check for spelling, typoes, etc..

# Attacks

* Re-entrancy attack: [https://hackernoon.com/hack-solidity-reentrancy-attack](https://www.certik.com/resources/blog/1eFmMTGVicfAMiPka3vaTY-cross-function-reentrancy-attacks-in-kadena-smart-contracts)

# Functional tests

Using REPL to implement and simulate the functional testing: https://docs.kadena.io/build/pact/atom-sdk

```
;; ========================================================
;;                                       1-load-environment-data
;; ========================================================
 
"Loading loans.repl..."
"Setting transaction keys"
"Setting transaction data"
""
""
;; ========================================================
;;                                        2-load-pact-file
;; ========================================================
 
"Loading loans.pact..."
"Keyset defined"
"Loaded module \"loans\", hash \"552198d5bc3a6cf8e84919a1b0f8c5cc764f65455e8dc687e3b6680b225e2684801fbfd42d6c734f798e3e210a03d5c9d6100c74433e3e16428903c95292466e\""
"TableCreated"
"TableCreated"
"TableCreated"
""
""
""
""
;; ========================================================
;;                                         3-call-functions
;; ========================================================
 
 
"Using \"loans\""
"Write succeeded"
"Write succeeded"
"Write succeeded"
"Write succeeded"
""
""
""
""
 
;; ========================================================
;;                                          4-read-loans
;; ========================================================
 
"Using \"loans\""
[{"inventory-key": "loanId-1:Capital One", "balance": 40000} {"inventory-key": "loanId-1:buyer1", "balance": 6000} {"inventory-key": "loanId-1:buyer2", "balance": 2000} {"inventory-key": "loanId-1:buyer3", "balance": 2000}]
[]
[{"entityName": "Capital One", "loanAmount": 50000, "loanName": "loan1", "status": "assigned"}]
""
""
 
```

