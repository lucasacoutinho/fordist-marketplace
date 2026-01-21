# Fordist

Assembly-line production of reusable development knowledge.

## Philosophy

Just like Ford's assembly line broke complex car manufacturing into repeatable, reusable components - Fordist breaks development knowledge into repeatable, reusable skills.

```
Build Feature → /retrospective → Skill created locally
                                        ↓
                              /publish → Skill added to Fordist
                                        ↓
                              Anyone installs Fordist → Knowledge flows everywhere
```

## Installation

```bash
claude plugins add github:lucasacoutinho/fordist-marketplace
```

Or add to `~/.claude/settings.json`:

```json
{
  "enabledPlugins": {
    "fordist@fordist-marketplace": true
  }
}
```

## Usage

### Capture Knowledge

After completing a feature, use `/retrospective` to capture what you learned:

```
/retrospective
```

This creates a skill in your project's `.claude/skills/features/` directory.

### Publish to Fordist

Share your skill with all your projects:

```
/publish
```

This copies the skill to the Fordist marketplace and pushes to GitHub.

### Find Past Work

Before starting a new feature, search for relevant skills:

```
/advise authentication
```

This searches both project-local skills and the Fordist marketplace.

## Core Skills

| Skill | Description |
|-------|-------------|
| `fordist:retrospective` | Document completed features as reusable skills |
| `fordist:advise` | Search project knowledge before starting work |

As you use `/retrospective` and `/publish`, more skills will appear here.

## Contributing

1. Build a feature in any project
2. Run `/retrospective` to capture the knowledge
3. Run `/publish` to add it to this marketplace
4. Create a PR if you want to share with others

## Inspiration

This project is inspired by the [AI Research Engineering Skills Library](https://huggingface.co/blog/AmberLJC/ai-research-engineering-skills) concept:

> "Think of `skills` as _invocable knowledge packages_—modular units that contain structured instructions, references, and resources for a specific domain."

The key insight is **separating lightweight reasoning from heavy resource retrieval** - loading knowledge on-demand rather than all at once. Fordist applies this principle to development knowledge: capture what you learn, retrieve it when relevant.

## License

MIT - see [LICENSE](LICENSE)
