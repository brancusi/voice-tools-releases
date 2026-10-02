# voice | pipes

A cowboy hacker's instrument for your Mac: hold a hotkey, talk, and your words run through a pipeline you laid
yourself (on-device transcription, your vocabulary, a model or two), then out at the cursor.

**[Download Voice Pipes](https://github.com/brancusi/voice-tools-releases/releases/latest/download/Voice-Pipes.dmg)**
· Apple silicon · macOS 14 or later · signed and notarized by Apple

## Install

1. Open **Voice-Pipes.dmg** and drag **Voice Pipes** onto **Applications**.
2. Open Voice Pipes. It lives in the menu bar.
3. **Set up Voice Pipes** walks you through the rest: Microphone and Accessibility permissions, the on-device
   models (they download in the background), and optional API keys for cloud steps.

**From a terminal**, or for an agent: the app, the `vp` command-line tool and the agent skill, with no prompts.

```sh
curl -fsSL https://github.com/brancusi/voice-tools-releases/releases/latest/download/install.sh | bash
```

It only installs a copy signed by Voice Pipes' developer and notarized by Apple. Add `-s -- --uninstall` to remove
it (your config, history and keys stay), or `-s -- --help` for the options.

After that it keeps itself up to date: when a new version is out, the menu bar panel offers **Install…**.

## What it does

| Track | Hotkey | Pipeline |
|---|---|---|
| Fast dictation | ⌥ Space, hold | Microphone › Parakeet v3 on your Mac › Fix words › Paste |
| Clean dictation | ⌥ ⇧ Space, toggle | Microphone › cloud transcription › Fix words › LLM cleanup › Paste |
| Read aloud | ⌥ R, toggle | Selected text › Pocket TTS on your Mac |

Every track is a row of blocks you can rearrange, swap or add to: transcription on your Mac or any OpenRouter
model, any LLM with your own instructions, Jev routing between models, HTTP requests, templates, speech from
on-device or cloud voices. Train your vocabulary once and names stop coming out wrong.

## Local first

Fast dictation and Read aloud run entirely on your Mac. Cloud steps (cleanup, cloud transcription, Q&A) only send
the text or audio of that step, with your own OpenRouter or TypeSafe key, stored in your Keychain.

This repository holds only the releases and the update feed the app checks. Release notes are on each
[release](https://github.com/brancusi/voice-tools-releases/releases).
