# Release v5.0.0 Checklist

## New Content Summary
- **Commands**: 148 → 216 (+68 new commands)
- **Skills**: 2 → 12 (+10 new skills)
- **AI Agents**: 54 (unchanged)
- **New Namespaces**: `webmcp/`, `media/`, `session/` + expanded `rust/`, `dev/`, `setup/`, `spec-workflow/`

## Tasks

- [x] Update README badge counts (216 commands, 12 skills)
- [x] Add new namespace sections to README
- [x] Add new dev namespace commands to README
- [x] Add new rust namespace commands to README
- [x] Add new project namespace commands to README
- [x] Add new skills to README Skills section
- [x] Update Table of Contents and navigation
- [x] Organize standalone files into namespace directories
- [x] Update README paths after reorganization
- [ ] Final review of README for accuracy

## Directory Reorganization

Files were moved from root `.claude/commands/` into proper namespace directories:

| Original Location | New Location | Namespace |
|---|---|---|
| `webmcp.md`, `webmcp-*.md` | `webmcp/` | `/webmcp:*` |
| `elevenlabs-transcribe.md`, `extract-video-frames.md` | `media/` | `/media:*` |
| `handoff.md`, `handoff-continue.md` | `session/` | `/session:*` |
| `setup-agent-tail.md`, `setup-portless.md` | `setup/` | `/setup:*` |
| `cleanup-vibes.md`, `remove-dead-code.md`, `create-ui-component.md`, `watch.md`, `xml-prompt-formatter.md` | `dev/` | `/dev:*` |
| `quick-spec.md`, `spec-elicitation.md` | `spec-workflow/` | `/spec-workflow:*` |

## New Commands by Namespace

### `/webmcp:*` (5 commands - NEW namespace)
| Command | Description |
|---------|-------------|
| `/webmcp:webmcp` | WebMCP umbrella command (setup, add-tool, debug, audit, test) |
| `/webmcp:setup` | Set up WebMCP from scratch |
| `/webmcp:add-tool` | Add a new WebMCP tool |
| `/webmcp:debug` | Debug WebMCP tools |
| `/webmcp:audit` | Audit WebMCP implementation |

### `/media:*` (2 commands - NEW namespace)
| Command | Description |
|---------|-------------|
| `/media:elevenlabs-transcribe` | Transcribe audio/video using ElevenLabs Scribe v2 |
| `/media:extract-video-frames` | Extract PNG frames and audio segments from video |

### `/session:*` (2 commands - NEW namespace)
| Command | Description |
|---------|-------------|
| `/session:handoff` | Create comprehensive context handoff documents |
| `/session:handoff-continue` | Handoff + spawn new Claude session in Zellij pane |

### `/dev:*` (+10 commands)
| Command | Description |
|---------|-------------|
| `/dev:incremental-feature-build` | Build features incrementally with validation gates |
| `/dev:parallel-feature-build` | Build features using parallel agent execution |
| `/dev:cloudflare-worker` | Generate and deploy Cloudflare Workers |
| `/dev:generate-linear-worklog` | Generate work logs from Linear task history |
| `/dev:rule2hook` | Convert CLAUDE.md rules to Claude Code hooks |
| `/dev:cleanup-vibes` | Transform vibecoded projects into structured codebases |
| `/dev:remove-dead-code` | Multi-agent dead code scanning with backup branches |
| `/dev:create-ui-component` | Create UI components with design system compliance |
| `/dev:watch` | File watcher triggering Claude on changes |
| `/dev:xml-prompt-formatter` | Reformat prompts using structured XML tags |

### `/setup:*` (+2 commands)
| Command | Description |
|---------|-------------|
| `/setup:agent-tail` | Configure agent-tail log aggregation |
| `/setup:portless` | Set up Portless for named `.localhost` URLs |

### `/spec-workflow:*` (+2 commands)
| Command | Description |
|---------|-------------|
| `/spec-workflow:quick-spec` | Rapid spec with opinionated codebase analysis |
| `/spec-workflow:spec-elicitation` | Full specification elicitation workflow |

### `/rust:*` (+20 commands - NEW namespace)
| Command | Description |
|---------|-------------|
| `/rust:audit-clean-arch` | Audit Rust codebase against Clean Architecture |
| `/rust:audit-dependencies` | Audit dependency direction violations |
| `/rust:audit-layer-boundaries` | Verify architectural layer boundaries |
| `/rust:audit-ports-adapters` | Audit Ports & Adapters pattern compliance |
| `/rust:suggest-refactor` | Generate refactoring suggestions |
| `/rust:setup-tauri-mcp` | Setup Tauri MCP integration |
| `/rust:tauri:launch` | Launch Tauri application |
| `/rust:tauri:health` | Check Tauri app health |
| `/rust:tauri:inspect` | Inspect Tauri app state |
| `/rust:tauri:screenshot` | Capture Tauri app screenshots |
| `/rust:tauri:call-ipc` | Call Tauri IPC commands |
| `/rust:tauri:list-commands` | List available IPC commands |
| `/rust:tauri:exec-js` | Execute JavaScript in Tauri webview |
| `/rust:tauri:click` | Click elements in Tauri UI |
| `/rust:tauri:type` | Type text into Tauri UI |
| `/rust:tauri:window` | Manage Tauri windows |
| `/rust:tauri:devtools` | Open Tauri DevTools |
| `/rust:tauri:logs` | View Tauri application logs |
| `/rust:tauri:resources` | Manage Tauri app resources |
| `/rust:tauri:stop` | Stop running Tauri application |

### Other Additions (+4 commands)
| Command | Description |
|---------|-------------|
| `/project:todo-branch` | Create feature branches from todo items |
| `/project:todo-worktree` | Create git worktrees from todo items |
| `/orchestration:log` | View task activity and change history |
| `/memory:prune` | Remove stale or irrelevant memories |

## New Skills Added (10)

| Skill | Domain | Description |
|-------|--------|-------------|
| `webmcp` | AI/Browser | WebMCP browser-native AI tool integration |
| `bigcommerce-api` | E-commerce | BigCommerce REST/GraphQL API expert |
| `audit-env-variables` | Security | Environment variable auditing and cleanup |
| `remove-dead-code` | Code Quality | Multi-agent dead code detection and removal |
| `elevenlabs-transcribe` | Audio/AI | ElevenLabs Scribe v2 transcription |
| `extract-video-frames` | Video/AI | Video frame and audio extraction via ffmpeg |
| `file-watcher` | Dev Tooling | Chokidar-based file change watcher |
| `gsap-animation` | Animation | GSAP API reference and cheatsheet |
| `setup-agent-tail` | Dev Tooling | Agent-tail log aggregation setup |
| `setup-portless` | Dev Tooling | Portless named .localhost URL setup |
