# Plugin Trust Promotion Decision Card

Status: template-ready; no validation proof recorded yet.

Package: [[Agent Plugin Marketplace Trust Kit]]  
Source packet: [[Agent Plugin Marketplace Trust Kit/Plugin Trust Review Packet]]

## When to fill this
Use this card only after the Plugin Trust Review Packet has been filled for one real marketplace plugin, MCP server, skill pack, command bundle, or agent extension. Do not infer safety from marketplace presence alone.

## Evidence links
| Required proof | Link / path | Notes |
|---|---|---|
| Plugin listing, repo, package, or manifest URL |  |  |
| Declared capabilities and requested permissions |  |  |
| Install/runtime commands reviewed |  |  |
| Filesystem, network, secret, and tool access notes |  |  |
| Sandbox/dry-run transcript or log |  |  |
| Human reviewer note |  |  |

## Decision gate
Choose exactly one after evidence is attached.

- [ ] **Install** — source is credible, permissions are bounded, sandbox run is clean, and rollback path is documented.
- [ ] **Sandbox only** — useful plugin, but trust boundary requires isolated profile/container or read-only credentials.
- [ ] **Iterate review** — packet lacks proof, manifest is ambiguous, or new permission categories must be added.
- [ ] **Reject** — provenance, permissions, command behavior, or maintenance risk is unacceptable.

## Trust criteria
| Criterion | Pass/Fail | Evidence link |
|---|---|---|
| Source identity and maintenance status are inspectable |  |  |
| Requested permissions match declared capabilities |  |  |
| Install commands do not hide unexpected network/code execution steps |  |  |
| Sandbox plan protects secrets, repos, and Hermes profile state |  |  |
| Decision is reversible with clear uninstall/rollback notes |  |  |

## Follow-up patch queue
- [ ] Patch `Artifacts/Skills/agent-plugin-trust-review/SKILL.md` with trial-backed pitfalls.
- [ ] Update the package README with the real trust decision summary.
- [ ] Add a filled review example only if every claim has a source link.
- [ ] Update [[Agent Plugin Marketplace Trust Kit Loop]] with the final install / sandbox / iterate / reject result.

## Guardrail
Do not mark the kit validated, safe, or promotion-ready until every claim above points to a packet row, manifest, repo link, sandbox log, permission diff, or reviewer note.
