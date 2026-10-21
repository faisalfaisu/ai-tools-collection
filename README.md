# AI Tools Collection

A curated collection of AI tools and agent skills: video and animation, voice, personal agents, coding helpers and design. Every entry links to the official repository and its documented install method.

Documentation for each project was checked on 17-20 October 2026 (latest additions 20 October). The tools are not independently tested here, so read each repo's own README before running anything - agent skills can run code on your machine.

About cost: the code in every listed repo is free unless noted, but your own AI assistant usage (Claude Pro, API credits) is separate, and a few tools need paid third-party APIs. Those are flagged in the Licence / cost column.

## Video and animation skills (for Claude Code and similar agents)

| Tool | What it does | Install | Licence / cost |
|---|---|---|---|
| [HyperFrames](https://github.com/heygen-com/hyperframes) | Coded motion-graphics videos rendered locally with Chrome + FFmpeg; captions and audio | `npx skills add heygen-com/hyperframes` | Commercial use allowed |
| [Lemo-Opuscar](https://github.com/lemomo-ai/lemo-opuscar) | 51 ready film styles; the agent directs a short film in code. Needs Node 20+, FFmpeg, Python 3.11+; Windows via WSL | `claude plugin marketplace add lemomo-ai/lemo-opuscar` then `claude plugin install lemo-opuscar@lemolab` | MIT |
| [Anatomy](https://github.com/wheresryan22/anatomy) | Interactive isometric "how a machine works" explainers | `npx skills add wheresryan22/anatomy -g -a claude-code` | MIT |
| [Remotion skills](https://github.com/remotion-dev/skills) | Official skills for Remotion, the React video framework | `npx skills add remotion-dev/skills` | Free code |
| [Remotion Video Director](https://github.com/BayramAnnakov/remotion-video-director) | Community director skill: brief, scenes, build, review | `npx skills add BayramAnnakov/remotion-video-director` | Free code |
| [Explanimate](https://github.com/notpritam/explanimate) | React/SVG animated explainers exported to MP4. Very new; needs Node 22+, pnpm, Playwright | `git clone https://github.com/notpritam/explanimate.git` then link into your skills folder (see its INSTALL.md) | Free code |
| [Manim skill](https://github.com/adithya-s-k/manim_skill) | Diagram and maths animation patterns (Manim). Needs Python, FFmpeg, LaTeX | `npx skills add adithya-s-k/manim_skill` | Free code |
| [Blender education video skill](https://github.com/sunxiayi/make-blender-education-video-skill) | 3D educational videos in Blender, with a preview-approval step | Clone the repo, copy `skills/make-blender-education-video` into `~/.claude/skills/` | Free code |
| [cc-blender-skill](https://github.com/RobLe3/cc-blender-skill) | 30 Blender helper skills through BlenderMCP (Blender 4.0+) | Clone, then symlink `plugin/skills/*` into `~/.claude/skills/` | Free code |
| [ReelMimic](https://github.com/edenfunf/reelmimic) | Local app: analyses a reference video's editing style, then makes a new video in that style. Needs Git, Node 22.18+, Python 3.10+, FFmpeg, Chrome, Claude Code | `git clone https://github.com/edenfunf/reelmimic.git` then run `install.bat` (Windows) or `./install.sh` | Free code |
| [html-anime](https://github.com/blixvip/html-anime) | Guides an agent to draw stylised anime scenes in HTML, rendered as video through HyperFrames | `git clone https://github.com/blixvip/html-anime.git` then serve with `python -m http.server` | Free code |
| [OpenMontage](https://github.com/calesthio/openmontage) | A coding assistant handles script, assets, narration, captions and render. Needs Python 3.10+, FFmpeg, Node 18+ | `git clone https://github.com/calesthio/OpenMontage.git` then `cd OpenMontage && make setup` | Free code; its demo films used paid generation APIs, and a free path with free stock footage is documented |
| [Claude Animation Base](https://github.com/JohnHeibel/ClaudeAnimationBase) | Hand-painted 2D cartoon starter kit (p5.js, 31 emotions). Landscape canvas by default | `git clone https://github.com/JohnHeibel/ClaudeAnimationBase.git` then `cd ClaudeAnimationBase && npm install` | MIT |
| [EffectCraft](https://github.com/storytold/effectcraft) | Standalone app, not a skill: open-source After Effects alternative. Early alpha | Installers for Windows, Mac and Linux: https://github.com/storytold/effectcraft/releases | MIT / Apache-2.0 |
| [GSAP skills](https://github.com/greensock/gsap-skills) | Official GSAP skills: web animation polish and easing (web pages, not video export) | `npx skills add greensock/gsap-skills -g` | Free code |
| [Youtube-clipper skill](https://github.com/op7418/Youtube-clipper-skill) | Clips and prepares YouTube footage for editing | `npx skills add op7418/Youtube-clipper-skill` | Free code |
| [Claude Motion Design](https://github.com/howseen-ai/claude-motion-design) | Motion graphics in HTML rendered to MP4 with Chromium + FFmpeg; no paid API needed. Windows support unconfirmed | Manual install - follow the repo README | Free code |
| [Diffusion Studio](https://github.com/diffusionstudio/editor) | Real-footage video editor that links to Claude Code; Windows build available | App download and setup in the repo README | Free code |
| [Wan2GP](https://github.com/deepbeepmeep/Wan2GP) | Local AI video generation on Windows; some models run with as little as 6 GB of GPU VRAM | Windows install documented in the repo README; needs an NVIDIA GPU | Check the repo licence before use |
| [Remotion](https://github.com/remotion-dev/remotion) | The React video framework itself - make real videos in code (the Remotion skills above teach an agent to drive it) | Official project starter - see the repo README | Free for individuals and small teams; larger companies need a paid licence |
| [Motion Canvas](https://github.com/motion-canvas/motion-canvas) | Animations and diagrams in code, timed to narration | Official project starter - see the repo README | MIT |

### Animation and video libraries (ingredients, not agent skills)

These came from a shared reel. They are building blocks an agent can use inside a video or web project; install each one only when a project needs it.

| Tool | What it does | Install | Licence / cost |
|---|---|---|---|
| [GSAP](https://github.com/greensock/GSAP) | Smooth timeline and text animation for web pages | `npm install gsap` | Free, including commercial use |
| [Anime.js](https://github.com/juliangarnier/anime) | Lightweight web and interface animation | `npm install animejs` | MIT |
| [Rive](https://github.com/rive-app/rive-wasm) | Interactive animation runtime for web and apps | `npm install @rive-app/canvas` | Runtime MIT; the Rive editor needs a paid plan to export .riv files |
| [Three.js](https://github.com/mrdoob/three.js) | 3D scenes in the browser | `npm install three` | MIT |
| [React Three Fiber](https://github.com/pmndrs/react-three-fiber) | Three.js through React components | `npm install @react-three/fiber` | MIT |
| [Satori](https://github.com/vercel/satori) | Static SVG title cards from HTML-like code (images, not video) | `npm install satori` | MPL-2.0 |
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

## Coding helpers and model routing

| Tool | What it does | Install | Licence / cost |
|---|---|---|---|
| [Skills CLI](https://github.com/vercel-labs/skills) | The `npx skills add` installer used by most skills in this list; includes the find-skills skill | `npx skills add https://github.com/vercel-labs/skills` | Free code |
| [9Router](https://github.com/decolua/9router) | Routes between AI providers with fallback. Video claims of "unlimited free Claude" are overstated | `npm install -g 9router` | Free code |
| [OmniRoute](https://github.com/diegosouzapw/OmniRoute) | Puts many free-tier AI APIs behind one local endpoint | `npm install -g omniroute` | Free code |
| [rea](https://github.com/morluto/rea) | Reverse-engineering toolkit for agents. Install only from morluto/rea or rea.tools (its own warning); needs Node 22, 24 or 26 (24.11+ in the 24.x line) | `npx rea-agents@latest setup` - during setup select your agent (for example Claude Code), review the changes and approve | Free code; optional Hopper install can be skipped |
| [Claude Code Templates](https://github.com/davila7/claude-code-templates) | Collection of agents, commands, hooks and project templates for Claude Code. Pick add-ons for a specific problem; don't install everything | `npx claude-code-templates@latest` | Free code; some add-ons connect to paid services or need separate API keys |

## Design and UI skills

| Tool | What it does | Install | Licence / cost |
|---|---|---|---|
| [Design DNA](https://github.com/zanwei/design-dna) | Agent analyses a reference design's layout, fonts and colours | `npx skills add zanwei/design-dna -a claude-code -g -y` | MIT |
| [UI/UX Pro Max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | UI/UX skill pack for many coding assistants | `npm install -g ui-ux-pro-max-cli` then `uipro init --ai claude` | Free code |
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

---

Notes:
- Install commands come from each project's own README, checked 17-20 October 2026. These projects move fast; if a command fails, check the repo first.
- `npx skills add` is the Skills CLI; its newer versions ask for Node.js 22.20 or later (per the Anatomy repo's README).
- Ignore star counts quoted in reels and videos; judge by features, licence and cost.
