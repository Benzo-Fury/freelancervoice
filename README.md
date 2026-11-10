# FreelancerVoice

A Claude skill that writes warm-but-firm replies from freelancers to clients. It covers discount requests, free or spec work, scope creep, rush jobs, late payment, ghosting and more, and it protects your time, scope and rate without damaging the relationship.

## Credit

The voice, principles and scripts in this skill come from **Jamie Brindle** ([@thejamiebrindle](https://www.instagram.com/thejamiebrindle/), [YouTube](https://www.youtube.com/@thejamiebrindle)). He's a freelancing educator who teaches creatives how to talk to clients. This skill distills about 78 of his most-watched client-communication videos. The video IDs cited in `references/playbooks.md` link back to the source videos (`youtube.com/watch?v=<id>`).

This is an unofficial fan project. It is not affiliated with or endorsed by Jamie Brindle, and the skill is told never to present itself as him. If you find it useful, go follow and support his work. All credit for the ideas belongs to him.

## Install

**Any agent (Claude Code, Cursor, Codex, Gemini CLI and more)**, using the [skills CLI](https://skills.sh):
```bash
npx skills add Benzo-Fury/freelancervoice
```

**Claude Code plugin**: run these inside Claude Code:
```
/plugin marketplace add Benzo-Fury/freelancervoice
/plugin install freelancervoice@freelancervoice
```

**claude.ai / Claude desktop app**: download [`freelancervoice.zip`](https://github.com/Benzo-Fury/freelancervoice/raw/main/freelancervoice.zip), then go to Customize → Skills → Add → Upload a skill.

**Manual**: copy `skills/freelancervoice` into `~/.claude/skills/`.

## Usage

Paste a client message and ask for a reply, for example: *"Client says they found someone cheaper, how do I respond?"* The skill picks the matching playbook and drafts a short reply. You may also get one alternative version and a "check before sending" note.

## Structure
```
skills/freelancervoice/
├── SKILL.md                 # voice, core beliefs, reply structure, playbook index
└── references/playbooks.md  # 21+ situations with example replies
.claude-plugin/              # Claude Code plugin + marketplace manifests
freelancervoice.zip          # packaged for claude.ai upload
```

## Rebuilding the zip
```bash
cd skills && rm -f ../freelancervoice.zip && zip -r ../freelancervoice.zip freelancervoice -x '.*'
```

## How it was built
1. Listed his YouTube uploads by view count and filtered them for client topics.
2. Transcribed the audio locally with Whisper and labeled the speakers (client, freelancer, mentor).
3. Kept the 78 client-communication videos and distilled their recurring principles and scripts into the skill.
4. Tested the skill on sample client messages and refined it.

No transcripts or media are included in this repo.
