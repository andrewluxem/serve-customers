# serve-customers

Traces a supplied decision to customer evidence, affected groups, tradeoffs, and measures.

It produces:

- **Customer Impact Review:** a working artifact built from supplied facts, labeled inference, and visible missing fields.

It executes the [Serve Customers playbook](https://www.andrewluxem.com/playbooks/serve-customers). The playbook teaches the framework. This skill runs it and returns a working artifact.

**Static by construction: no dependencies, executable code, telemetry, network calls, remote instructions, auto-update, scheduled work, or background behavior.** It reads only the files in its own skill folder. Nothing happens until a user or agent invokes it.

## Install

Clone and copy the skill into Claude Code:

```bash
git clone https://github.com/andrewluxem/serve-customers.git
cp -r serve-customers/skills/serve-customers ~/.claude/skills/
```

For Codex, copy the same complete folder to the Codex skills directory:

```bash
cp -r serve-customers/skills/serve-customers ~/.codex/skills/
```

Or install it as a Claude Code plugin:

```text
/plugin marketplace add andrewluxem/serve-customers
/plugin install serve-customers@serve-customers
```

For clients that install from an archive, use the versioned [serve-customers v1.0.0 ZIP](https://www.andrewluxem.com/downloads/serve-customers-v1.0.0.zip).

## Invoke it

```text
Check this plan against customer impact
Use the serve-customers skill.
```

Naming the skill is always valid: `use the serve-customers skill`.

## Files

```text
.claude-plugin/
  plugin.json
  marketplace.json
skills/serve-customers/
  assets/customer-impact-review-template.md
  LICENSE.md
  meta.yaml
  references/customer-impact-standard.md
  SKILL.md
README.md
LICENSE
```

The complete canonical package is copied under `skills/serve-customers/`, including every asset, reference, test prompt, source note, changelog entry, and license file present in the source.

## Versioning

Plugin installation is version-pinned. When behavior changes, update the version consistently in `SKILL.md`, `meta.yaml`, `.claude-plugin/plugin.json`, and `.claude-plugin/marketplace.json`, then add a changelog entry. Reinstalling is an explicit update; this repository never auto-updates itself.

## License

MIT. See [LICENSE](LICENSE). The canonical skill folder carries the same authorization in [skills/serve-customers/LICENSE.md](skills/serve-customers/LICENSE.md).
