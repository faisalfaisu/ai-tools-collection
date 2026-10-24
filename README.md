# AI Tools Collection

A curated collection of AI tools and agent skills: video and animation, voice, personal agents, coding helpers and design. Every entry links to the official repository and its documented install method.

Documentation for each project was checked on 17-20 October 2026 (latest additions 20 October). The tools are not independently tested here, so read each repo's own README before running anything - agent skills can run code on your machine.

About cost: the code in every listed repo is free unless noted, but your own AI assistant usage (Claude Pro, API credits) is separate, and a few tools need paid third-party APIs. Those are flagged in the Licence / cost column.

## Video and animation skills (for Claude Code and similar agents)

| Tool | What it does | Install | Licence / cost |
|---|---|---|---|
| [HyperFrames](https://github.com/heygen-com/hyperframes) | Coded motion-graphics videos rendered locally with Chrome + FFmpeg; captions and audio | `npx skills add heygen-com/hyperframes` | Commercial use allowed |
| [Lemo-Opuscar](https://github.com/lemomo-ai/lemo-opuscar) | 59 ready film styles; the agent directs a short film entirely in code (rendered frames, local Kokoro narration, music from free sample libraries). Styles tuned for Claude Opus 5.5 - other models may not reproduce them. Default output 1920x1080 landscape; vertical 1080x1920 on request. A film takes the agent about 30-60 minutes and a fair amount of tokens. Needs Node 20+, FFmpeg, Python 3.11+; Windows via WSL (untested) | `claude plugin marketplace add lemomo-ai/lemo-opuscar` then `claude plugin install lemo-opuscar@lemolab` | Code MIT; demo films CC BY 4.0 with credit. Free local narration and music defaults; heavy agent token usage |
| [Anatomy](https://github.com/wheresryan22/anatomy) | Interactive isometric "how a machine works" explainers | `npx skills add wheresryan22/anatomy -g -a claude-code` | MIT |
| [Remotion skills](https://github.com/remotion-dev/skills) | Official skills for Remotion, the React video framework | `npx skills add remotion-dev/skills` | Free code |
| [Remotion Video Director](https://github.com/BayramAnnakov/remotion-video-director) | Community director skill: brief, scenes, build, review | `npx skills add BayramAnnakov/remotion-video-director` | Free code |
| [Explanimate](https://github.com/notpritam/explanimate) | React/SVG animated explainers exported to MP4. Very new; needs Node 22+, pnpm, Playwright | `git clone https://github.com/notpritam/explanimate.git` then link into your skills folder (see its INSTALL.md) | Free code |
| [Manim skill](https://github.com/adithya-s-k/manim_skill) | Diagram and maths animation patterns (Manim). Needs Python, FFmpeg, LaTeX | `npx skills add adithya-s-k/manim_skill` | Free code |
| [Blender education video skill](https://github.com/sunxiayi/make-blender-education-video-skill) | 3D educational videos in Blender, with a preview-approval step | Clone the repo, copy `skills/make-blender-education-video` into `~/.claude/skills/` | Free code |
| [cc-blender-skill](https://github.com/RobLe3/cc-blender-skill) | 30 Blender helper skills through BlenderMCP (Blender 4.0+) | Clone, then symlink `plugin/skills/*` into `~/.claude/skills/` | Free code |
| [ReelMimic](https://github.com/edenfunf/reelmimic) | Local app: analyses a reference video's editing style, then makes a new 2D animated video in that style (seven drawing engines: vector motion graphics, picture book, whiteboard doodle, anime cel and more - no live-action footage of real people). Needs Git, Node 22.18+, Python 3.10+, FFmpeg, Chrome, Claude Code | `git clone https://github.com/edenfunf/reelmimic.git` then run `install.bat` (Windows) or `./install.sh` | MIT (bundled third-party skills keep their own licences); runs on your existing Claude Code or Codex plan - no extra paid API |
| [html-anime](https://github.com/blixvip/html-anime) | Guides an agent to draw stylised anime scenes in HTML, rendered as video through HyperFrames | `git clone https://github.com/blixvip/html-anime.git` then serve with `python -m http.server` | Free code |
| [OpenMontage](https://github.com/calesthio/openmontage) | A coding assistant handles script, assets, narration, captions and render. Needs Python 3.10+, FFmpeg, Node 18+ | `git clone https://github.com/calesthio/OpenMontage.git` then `cd OpenMontage && make setup` | Free code; its demo films used paid generation APIs, and a free path with free stock footage is documented |
| [Claude Animation Base](https://github.com/JohnHeibel/ClaudeAnimationBase) | Hand-painted 2D cartoon starter kit (p5.js, 31 emotions). Landscape canvas by default | `git clone https://github.com/JohnHeibel/ClaudeAnimationBase.git` then `cd ClaudeAnimationBase && npm install` | MIT |
| [EffectCraft](https://github.com/storytold/effectcraft) | Standalone app, not a skill: open-source After Effects alternative. Early alpha | Installers for Windows, Mac and Linux: https://github.com/storytold/effectcraft/releases | MIT / Apache-2.0 |
| [GSAP skills](https://github.com/greensock/gsap-skills) | Official GSAP skills: web animation polish and easing (web pages, not video export) | `npx skills add greensock/gsap-skills -g` | Free code |
| [Youtube-clipper skill](https://github.com/op7418/Youtube-clipper-skill) | Clips and prepares YouTube footage for editing | `npx skills add op7418/Youtube-clipper-skill` | Free code |
| [Claude Motion Design](https://github.com/howseen-ai/claude-motion-design) | Motion graphics in HTML rendered to MP4 with Chromium + FFmpeg; no paid API needed. Windows support unconfirmed | Manual install - follow the repo README | Free code |
| [Diffusion Studio](https://github.com/diffusionstudio/editor) | Real-footage video editor that links to Claude Code; Windows build available | App download and setup in the repo README | Free code |
| [Wan2GP](https://github.com/deepbeepmeep/Wan2GP) | Local AI video generation on Windows; some models run with as little as 6 GB of GPU VRAM | Windows install documented in the repo README; needs an NVIDIA GPU | WanGP Community License 2.0 (custom): free including commercial use; you can sell generated videos, crediting WanGP when you sell an output directly; you cannot sell, white-label or embed the app itself in a paid product. Bundled models keep their own licences |
| [Remotion](https://github.com/remotion-dev/remotion) | The React video framework itself - make real videos in code (the Remotion skills above teach an agent to drive it) | Official project starter - see the repo README | Free for individuals and small teams; larger companies need a paid licence |
| [Motion Canvas](https://github.com/motion-canvas/motion-canvas) | Animations and diagrams in code, timed to narration | Official project starter - see the repo README | MIT |
| [Brag](https://github.com/latent-spaces/brag) | Agent skill that turns an app or website project into a short launch-promo video (about 20 seconds: motion, music, share copy) - product promos, not general story videos. brag-slim (built for Opus 5.5) needs no extra tools; the classic workflow needs FFmpeg and the HyperFrames CLI, with a Windows symlink caveat (manual copy fallback documented) | brag-slim: `npx skills add https://github.com/latent-spaces/brag --skill brag-slim`; classic in Claude Code: `/plugin marketplace add latent-spaces/brag` then `/plugin install brag@brag` | MIT (code; the bundled music tracks' licence is unverified). Runs on your Claude plan usage; letsbrag.app is a separate paid hosted service |

### Animation and video libraries (ingredients, not agent skills)

These came from a shared reel. They are building blocks an agent can use inside a video or web project; install each one only when a project needs it.

| Tool | What it does | Install | Licence / cost |
|---|---|---|---|
| [GSAP](https://github.com/greensock/GSAP) | Smooth timeline and text animation for web pages | `npm install gsap` | Free, including commercial use |
| [Anime.js](https://github.com/juliangarnier/anime) | Lightweight web and interface animation | `npm install animejs` | MIT |
| [Motion](https://github.com/motiondivision/motion) | Web and React animation library (formerly Framer Motion) | `npm install motion` | MIT; optional Motion+ add-ons are paid |
| [Rive](https://github.com/rive-app/rive-wasm) | Interactive animation runtime for web and apps | `npm install @rive-app/canvas` | Runtime MIT; the Rive editor needs a paid plan to export .riv files |
| [Three.js](https://github.com/mrdoob/three.js) | 3D scenes in the browser | `npm install three` | MIT |
| [React Three Fiber](https://github.com/pmndrs/react-three-fiber) | Three.js through React components | `npm install @react-three/fiber` | MIT |
| [Satori](https://github.com/vercel/satori) | Static SVG title cards from HTML-like code (images, not video) | `npm install satori` | MPL-2.0 |
| [ThreeUI](https://github.com/MengTo/threeui) | Three.js / WebGL / React landing-page templates, hero sections and shader components with editable source - website UI, not video editing | `npm install @designcodeio/threeui` | Community library MIT (164 free components, no login; bundled fonts under SIL OFL 1.1); the full ThreeUI Pro catalog is a separate paid plan ($199/year or $299 lifetime at time of checking) |
| [FFmpeg](https://github.com/FFmpeg/FFmpeg) | Video export, encoding and resizing - the engine many tools here rely on | Windows builds from ffmpeg.org, or `winget install ffmpeg` | LGPL/GPL - read the licence for distribution |

## Voice and narration apps

| Tool | What it does | Install | Licence / cost |
|---|---|---|---|
| [VoiceStudio](https://github.com/debpalash/VoiceStudio) | Local voice cloning, narration, dubbing and transcription. Windows; needs several GB of disk for models | Windows installer (.exe): https://github.com/debpalash/VoiceStudio/releases (one-line PowerShell installer also documented) | Free code |
| [Voicebox](https://github.com/jamiepine/voicebox) | Local text-to-speech and voice cloning with 8 engines | Windows/Mac/Linux installers: https://github.com/jamiepine/voicebox/releases or https://voicebox.sh | MIT |

## AI agents and assistants

| Tool | What it does | Install | Licence / cost |
|---|---|---|---|
| [nanoMuse](https://github.com/nano-muse/nanoMuse) | Open-source personal agent for iPhone (TestFlight), Android, Windows, Mac and browser | Installers: https://github.com/nano-muse/nanoMuse/releases | GPL-3.0; its docs describe a limited free community model allowance |
| [OpenClaw](https://github.com/openclaw/openclaw) | Personal agent that runs on your own computer and connects to WhatsApp, Telegram, Slack and more. Its unofficial WhatsApp linking can put your number at risk | `npm install -g openclaw@latest --allow-scripts=openclaw` (Node 24.16+ or 26.1+) | MIT; model access required - provider costs and terms vary |
| [ZeroClaw](https://github.com/zeroclaw-labs/zeroclaw) | Single-binary Rust agent runtime with 30+ channels | Prebuilt installers for Windows, Mac and Linux: https://github.com/zeroclaw-labs/zeroclaw/releases | Free code; model access required - provider costs and terms vary |
| [nanobot](https://github.com/HKUDS/nanobot) | Python personal agent with a browser UI; Telegram, Discord, Slack and more | Follow the Install and Quick Start guide in the repo | Free code; model access required - provider costs and terms vary |
| [Windows-Use](https://github.com/Jeomon/Windows-Use) | Agent that controls a Windows PC (opens apps, clicks, types). Run it in a test folder first | `pip install windows-use` (Python 3.10+, Windows) | MIT; model access required (API key or local model) - provider costs and terms vary |
| [jcode](https://github.com/1jehuang/jcode) | Fast terminal coding agent in Rust; can run several agents on one project | Mac/Linux: `curl -fsSL https://jcode.sh/install \| bash`; Windows steps on jcode.sh | Free code; model access required - provider costs and terms vary |
| [Agent Reach](https://github.com/Panniantong/Agent-Reach) | Gives a coding agent extra web reading: web pages, YouTube subtitles/search and GitHub research. Its Instagram channel needs an optional extension plus a logged-in browser and is not part of the basic setup | Python: make a virtual environment, install the package from the repo's GitHub archive, then `agent-reach install --env=auto` (check-only) - full guide in the repo's docs/install.md | Free code |
| [Hermes Agent](https://github.com/NousResearch/hermes-agent) | Nous Research's self-improving personal agent: saved memory, skills it writes and improves itself, messaging on Telegram/Discord/Slack/WhatsApp/Signal, and scheduled jobs delivered to your chat. Runs natively on Windows or on a server (VPS optional; the host must stay awake and online for 24/7 use) | Windows PowerShell: `iex (irm https://hermes-agent.nousresearch.com/install.ps1)`; Linux/macOS: `curl -fsSL https://hermes-agent.nousresearch.com/install.sh \| bash` | MIT; model usage is separate - API providers bill on top, and an experimental option draws your logged-in Claude Code subscription allowance (not full parity, untested) |
| [Artemis](https://github.com/google/artemis) | Google's MCP server that lets an AI coding agent control a real Android phone or emulator from plain English - app automation, testing, Logcat output and screenshots. Android only; needs USB debugging or an emulator, and a model API key (Gemini by default - a free AI Studio tier exists, but some model options are paid or preview). It offers to install agent rules into your IDE - review them first | Clone the repo, then `.\start.bat` on Windows or `./start.sh` on macOS/Linux (auto-installs ADB, scrcpy, FFmpeg and uv) | Apache-2.0; model API usage billed separately. Its 99%+ AndroidWorld score is Google's own benchmark |

## Coding helpers and model routing

| Tool | What it does | Install | Licence / cost |
|---|---|---|---|
| [Skills CLI](https://github.com/vercel-labs/skills) | The `npx skills add` installer used by most skills in this list; includes the find-skills skill | `npx skills add https://github.com/vercel-labs/skills` | Free code |
| [9Router](https://github.com/decolua/9router) | Routes between AI providers with fallback. Video claims of "unlimited free Claude" are overstated | `npm install -g 9router` | Free code |
| [OmniRoute](https://github.com/diegosouzapw/OmniRoute) | Puts many free-tier AI APIs behind one local endpoint | `npm install -g omniroute` | Free code |
| [rea](https://github.com/morluto/rea) | Reverse-engineering toolkit for agents. Install only from morluto/rea or rea.tools (its own warning); needs Node 22, 24 or 26 (24.11+ in the 24.x line) | `npx rea-agents@latest setup` - during setup select your agent (for example Claude Code), review the changes and approve | Free code; optional Hopper install can be skipped |
| [Claude Code Templates](https://github.com/davila7/claude-code-templates) | Collection of agents, commands, hooks and project templates for Claude Code. Pick add-ons for a specific problem; don't install everything | `npx claude-code-templates@latest` | Free code; some add-ons connect to paid services or need separate API keys |
| [Vibe Coding Toolkit](https://github.com/soumatheusgomes/vibe-coding-toolkit) | Collection of documentation, prompts and templates that configure your machine and projects for AI coding agents (guides cover Claude Code and Codex): environment setup, project bootstrap, quality checks, memory | No installer - run its setup prompts from the repo README inside Claude Code or Codex; review each machine-configuring prompt before running it | MIT; its token-saving tools are unverified |
| [Gitingest](https://gitingest.com) | Turns any GitHub repo into a prompt-friendly text digest (file tree plus file contents) - replace "hub" with "ingest" in the repo URL | No install - hosted site; CLI: `pip install gitingest` | Free hosted; MIT |
| [github1s](https://github1s.com) | Opens any public GitHub repo in a VS Code-style reader in the browser (add "1s" after "github" in the URL); no sign-in needed. Remote repos are read-only - edits stay in the browser | No install - hosted site | Free; MIT |
| [GitDiagram](https://gitdiagram.com) | Turns a GitHub repo into an interactive architecture diagram - the diagrams are AI-generated approximations, not ground truth | No install - hosted site; self-hosting needs your own OpenAI or OpenRouter API key | Free hosted; MIT |
| [GitVerse](https://gitverse.id) | Turns a pasted codebase or repo into an architecture breakdown plus a copy-paste prompt to rebuild it in Claude or Cursor. New, small project - output quality untested | No install - hosted site; self-host from the repo (needs your own LLM API key) | Repo MIT; hosted cost and limits unverified (no pricing shown) |

## Design and UI skills

| Tool | What it does | Install | Licence / cost |
|---|---|---|---|
| [Design DNA](https://github.com/zanwei/design-dna) | Agent analyses a reference design's layout, fonts and colours | `npx skills add zanwei/design-dna -a claude-code -g -y` | MIT |
| [UI/UX Pro Max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | UI/UX skill pack for many coding assistants. Needs Python 3 for its search script | In Claude Code: `/plugin marketplace add nextlevelbuilder/ui-ux-pro-max-skill` then `/plugin install ui-ux-pro-max@ui-ux-pro-max-skill`; or `npm install -g ui-ux-pro-max-cli` then `uipro init --ai claude` | MIT |
| [Emil Kowalski's skills](https://github.com/emilkowalski/skills) | Animation easing and UI design guidance skills, including apple-design (UI motion and typography polish) | `npx skills@latest add emilkowalski/skills` | Free code |
| [Replica skills](https://github.com/Jakeschincariol/replica-skill) | Eleven skills that clone an app's design and rebuild it | In Claude Code: `/plugin marketplace add Jakeschincariol/replica-skill` | MIT |

## Vox-style explainer skills

| Tool | What it does | Install | Licence / cost |
|---|---|---|---|
| [vox-editorial](https://github.com/jaredcassoutt/vox-editorial) | Local Vox-style workflow: research, script, narration, layered images, captions. Needs FFmpeg, Python 3.10+ | Clone the repo into `~/.claude/skills/`; free narration via `edge-tts` | Free code; very new, small repo |
| [vox-director](https://github.com/Alisa0808/vox-director) | Collage-style explainers | `git clone https://github.com/Alisa0808/vox-director.git ~/.claude/skills/vox-director` | Code free; default workflow needs a separately billed Atlas Cloud API |

## Other repos and limitations

| Tool | Limitation |
|---|---|
| [onetake](https://github.com/feitangyuan/onetake) | One-take launch films; its licence is PolyForm Noncommercial, so commercial use is not covered - the project sells onetake Pro |
| [gbro-collage-broll](https://github.com/pyang5166/gbro-collage-broll) | Paper-collage B-roll; video generation needs a paid Gemini API key |
| [FreeVideo](https://github.com/FlashML-org/FreeVideo) | Local video model that needs about 8 GB of GPU VRAM; its licence has usage limits - check the repo |
| [OpenWA](https://github.com/rmyndharis/OpenWA) | Unofficial WhatsApp automation; its own repo warns about number bans |
| [gods-eye-view](https://github.com/bilawalsidhu/gods-eye-view) | Interactive 3D globe demo; not a workflow tool |
| [vgpu](https://github.com/vercel-labs/vgpu) | Shader experiments; reference material |
| [Meetily](https://github.com/Zackriya-Solutions/meetily) | Local meeting transcription app (MIT; Windows installer: https://github.com/Zackriya-Solutions/meetily/releases); a different category from the rest of this list |
| [OpenAlternative](https://github.com/piotrkulpinski/openalternative) | Directory website (openalternative.co) for finding open-source alternatives to paid software; browse without signing up |
| [awesome-opus5-5-videos](https://github.com/yihui-dev/awesome-opus5-5-videos) | Prompt gallery for short videos made with code animation (HTML Canvas, SVG, Three.js - not AI diffusion footage); its maintainer counts 700+ prompts with original-vs-remake pairs, free to read at skillry.dev/ai-videos/opus-5-5 with no account (optional premium separate). Reference only - prompts are not independently tested, and the MIT licence covers the list, not reposting the credited creators' videos |
| [21st.dev](https://21st.dev) | Marketplace of ready-made UI components for agent-built sites; browsing and search are free, the free tier allows 2 component code retrievals or installs a day; its AI generation features are paid |

---

Notes:
- Install commands come from each project's own README, checked 17-20 October 2026. These projects move fast; if a command fails, check the repo first.
- `npx skills add` is the Skills CLI; its newer versions ask for Node.js 22.20 or later (per the Anatomy repo's README).
- Ignore star counts quoted in reels and videos; judge by features, licence and cost.
