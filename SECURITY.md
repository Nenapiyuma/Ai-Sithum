# Security Policy

## Core rules

Ai-Sithum is local-first. Sensitive operations must not silently leave the local environment.

### Permission Gate

Any operation that can control the host computer, execute a command, modify files outside an explicitly selected workspace, install software, or perform another consequential action must require explicit user confirmation.

The execution boundary must:
- validate the requested action and target;
- fail closed when permission is absent, expired, malformed or ambiguous;
- never infer approval from a previous unrelated action;
- never execute in the background without an active permission state;
- require fresh confirmation for destructive or high-impact operations.

### Network

Offline mode must not silently fall back to cloud services. External requests require an explicit configuration path and should be visible to the user.

### Secrets

Do not commit API keys, access tokens, private keys, passwords or local credential stores. Use environment variables or platform secret stores.

### Model claims

A model configuration is not a model checkpoint. Documentation and UI must distinguish configured parameter counts from actually installed/trained weights.

### Reporting

Security issues should be reported privately to the repository owner before public disclosure.
