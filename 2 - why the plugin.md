# Why?

- The rule:
  - Intercept and log all input and output messages
  
- Reasons:
  - We are Humans and we will forget to add the logs
    - Could we create a lint rule for that? Yes...but...
  - The logs are verbose and repetitive work
  - Our new codebase is super clean
  - The codebase is small ~2193 loc
  - We knew exactly what to intercept