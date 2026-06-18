# Plugin Trust Evidence Quality Rubric

Purpose: grade the proof bundle from the next real plugin/extension review before changing README, prototype, or skill-draft claims. This is template-ready; no plugin has been validated yet.

Source: [[Grok Build Plugin Marketplace as Agent App Store]]  
Package: [[Agent Plugin Marketplace Trust Kit]]

## Minimum evidence bundle

| Evidence slot | Required before a trust claim changes | Link / note |
| --- | --- | --- |
| Real plugin target | Marketplace URL, repo URL, version, publisher, and install surface |  |
| Permission surface | Manifest, scopes, commands, hooks, MCP tools, or file/network access |  |
| Provenance check | Publisher identity, repo history, release tags, issue/security signals |  |
| Sandbox trial | Dry run, containerized test, denied-permission test, or safe mock install |  |
| Behavior trace | Logs, screenshots, transcript, network/file observations, or diff |  |
| Human review | Operator note explaining install / sandbox / iterate / reject decision |  |

## Scoring gate

- **Install / public claim ready:** all six slots filled, permissions are bounded, sandbox behavior matches the description, and no critical provenance gaps remain.
- **Sandbox-only:** four or five slots filled, utility is plausible, but provenance, permissions, or behavior still needs containment.
- **Iterate review:** two or three slots filled, useful learning captured, but trust is not established.
- **Reject / hold:** fewer than two slots filled or the permission/provenance risk is unacceptable.

## Claim patch checklist

- [ ] Evidence links copied into [[Agent Plugin Marketplace Trust Kit/Plugin Trust Evidence Index]].
- [ ] Decision copied into [[Agent Plugin Marketplace Trust Kit/Plugin Trust Promotion Decision Card]].
- [ ] Lessons copied into [[Agent Plugin Marketplace Trust Kit/Post-Trial Plugin Trust Debrief Template]].
- [ ] README/prototype/skill wording changed only if the scoring gate allows it.
