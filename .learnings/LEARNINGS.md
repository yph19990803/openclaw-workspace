# LEARNINGS.md

Structured log of corrections, knowledge gaps, and best practices.

## [LRN-20260327-001] best_practice

**Logged**: 2026-03-27T03:17:00Z
**Priority**: high
**Status**: pending
**Area**: config

### Summary
Do not ask for or use plaintext passwords or PATs in chat when setting up Git remotes; prefer SSH authentication.

### Details
The user shared a GitHub password and personal access token while trying to configure Git. Sensitive credentials should not be handled in chat for routine repository setup. SSH keys or credential managers are safer defaults for repeatable Git authentication.

### Suggested Action
Standardize on SSH-based Git remote setup. If a user shares a token/password in chat, advise rotation/revocation and avoid reusing or echoing the secret.

### Metadata
- Source: conversation
- Related Files: TOOLS.md
- Tags: security, git, ssh, credentials
- See Also: none

---
