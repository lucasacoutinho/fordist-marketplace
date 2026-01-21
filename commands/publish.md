---
name: publish
description: Publish a skill from this project to Fordist marketplace
---

# Publish to Fordist

Publish a skill to the Fordist marketplace for cross-project reuse.

## Workflow

1. List skills in `.claude/skills/features/`
2. Ask user which to publish (or accept argument)
3. Copy skill to `~/personal/fordist-marketplace/skills/<name>/`
4. Git add, commit, push
5. Confirm publication

## Steps

### Find publishable skills
```bash
find .claude/skills/features -name "SKILL.md" 2>/dev/null
```

### After user selects skill
1. Read `.claude/skills/features/<name>/SKILL.md`
2. Create directory `~/personal/fordist-marketplace/skills/<name>/`
3. Write skill to `~/personal/fordist-marketplace/skills/<name>/SKILL.md`
4. Run:
   ```bash
   cd ~/personal/fordist-marketplace
   git add skills/<name>
   git commit -m "feat(fordist): add <name> skill"
   git push
   ```

### Confirm
> Published `<name>` to Fordist. It will be available as `fordist:<name>` in all projects on next Claude Code session.

## Notes

- Skills are prefixed with `fordist:` when installed
- The marketplace repo must be set up at `~/personal/fordist-marketplace/`
- Ensure the skill has a proper SKILL.md with frontmatter (name, description)
