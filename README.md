# suno-automation — Browser-based Suno music generation via OpenClaw

> Control Suno's web interface through the OpenClaw managed browser — type lyrics, set style, generate, and play, all from agent commands.

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blueviolet)](https://github.com/NachaFromMars)

## Overview
suno-automation drives the Suno AI music creation interface through the OpenClaw managed browser. The agent navigates to suno.com/create, takes a browser snapshot to discover element references, fills in lyrics and style, submits the generation, and plays back the result — all through browser act commands. Requires the OpenClaw browser running and the user already logged into Suno on the managed profile.

## Features
- **Browser-driven** — uses OpenClaw managed browser, no API key
- **Snapshot-based** — `browser snapshot` reveals element refs for each field
- **Full workflow** — lyrics → style → title → create → play
- **Prerequisite** — OpenClaw browser running + Suno logged in on `openclaw` profile

## Usage / Quick Start
```
browser open https://suno.com/create
browser snapshot                          # get element refs
browser act type <lyric_ref> "lyrics"
browser act type <style_ref> "pop, upbeat"
browser act click <create_button_ref>
browser snapshot                          # find new song + play button
browser act click <play_button_ref>
```

## Trigger Keywords (OpenClaw)
suno, generate music with suno, suno automation, create song suno, browser suno

## Related Skills
- [suno-maker](https://github.com/NachaFromMars/suno-maker) — headless Linux server alternative
- [ai-songwriter](https://github.com/NachaFromMars/ai-songwriter) — API-based Suno alternative

---
Part of the [NachaFromMars](https://github.com/NachaFromMars) OpenClaw skill ecosystem.
