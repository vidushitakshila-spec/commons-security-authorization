# commons-security-authorization
1. Problem statement: Hardcoded role checks (@Secured("ROLE_ADMIN")) are too rigid for complex enterprise data ownership and fine-grained resource permissions.

2. Concepts and terminology: Attribute-Based Access Control (ABAC), Role-Based Access Control (RBAC), SpEL (Spring Expression Language) security expressions.

3. Available technologies / algorithms: Spring Security Method Security, Custom @PreAuthorize evaluators.

4. When to use what: Use for protecting service methods and database queries based on dynamic user attributes, tenant IDs, and fine-grained permissions.

5. Java APIs and dependencies: spring-security-aspects, Spring AOP, SpEL parser.

6. AWS equivalents: AWS Verified Permissions (Cedar policy engine), IAM Policies.

7. Architecture patterns: Policy Enforcement Point (PEP) / Policy Decision Point (PDP) separation, Aspect-Oriented Security.

8. Security considerations: Prevent SpEL injection vulnerabilities by never evaluating raw user input directly inside security expressions.

9. Implementation examples: Custom PermissionEvaluator checking record ownership via repository lookups.

10. References and further reading: NIST Guide to Access Control Technologies.
