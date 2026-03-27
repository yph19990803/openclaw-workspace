# ERRORS.md

Structured log of command failures, tool errors, and unexpected behavior.

## [ERR-20260327-001] read-skill-file-permission

**Logged**: 2026-03-27T03:09:00Z
**Priority**: medium
**Status**: pending
**Area**: config

### Summary
Reading the self-improvement skill file failed due to filesystem permission restrictions.

### Error
```
EACCES: permission denied, access '/root/.openclaw/skills/self-improving-agent/SKILL.md'
```

### Context
- Operation attempted: read skill file before following skill-specific instructions
- Target path: `/root/.openclaw/skills/self-improving-agent/SKILL.md`
- Environment detail: workspace access is available, but direct access to `/root/.openclaw/...` is restricted in this runtime

### Suggested Fix
When a skill path points to a restricted location, ask the user to paste the skill content or rely on copied content provided in chat. Do not assume all configured skill locations are readable.

### Metadata
- Reproducible: yes
- Related Files: none
- See Also: none

---
