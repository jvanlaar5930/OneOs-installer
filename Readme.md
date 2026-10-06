<p align="center">
  <img src="assets/orbit-logo.gif" alt="one_OS" width="400" />
</p>

<h1 align="center">One OS</h1>

<p align="center">
  <strong>A desktop that comes with no apps.</strong><br/>
  Describe the one you want and watch it appear.
</p>

<p align="center">
  <a href="https://github.com/jvanlaar5930/OneOs-installer/releases/latest"><img src="https://img.shields.io/github/v/release/jvanlaar5930/OneOs-installer?style=for-the-badge&label=Download%20for%20Windows&color=8a6bff" alt="Download for Windows"/></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platform-Windows_10%2F11_x64-0f1118?style=flat-square" alt="Platform"/>
  <img src="https://img.shields.io/badge/Claude_CLI-ready-8a6bff?style=flat-square" alt="Claude CLI"/>
  <img src="https://img.shields.io/badge/local_models-built_in-22c55e?style=flat-square" alt="Local models"/>
  <img src="https://img.shields.io/badge/OpenAI--compatible-API-5b9bff?style=flat-square" alt="OpenAI compatible"/>
</p>

---

Ever opened an app and found the one feature you need is missing? Every app you use was designed for someone else. The setting you want is buried or doesn't exist. The export button isn't there. You send a feature request and wait, or you pay for a second app that does that one thing, then a third. And the apps you depend on can change, raise their price or disappear without asking you.

one_OS works the other way round. It's a full desktop, with windows, a taskbar, files and a Start menu, and it comes with no apps. When you need one, you describe it, and the assistant writes it and puts it on your desktop. Missing a feature? Ask for it and it gets added. If you can describe it, you can have it.

Those apps are yours. They live on your machine, they work the way you want, and they only change when you ask.

```
"Make me a kanban board with swimlanes"
"Add a dark mode to it"
"Build me a platformer where the floor is lava"
"Remind me to stretch every 30 minutes"
```

## What you get

- **Apps that can't get lost.** Each app remembers everything you've asked for, so it can be rebuilt from scratch if an edit goes wrong.
- **Games, too.** Game Studio builds 2D and 3D games from a description.
- **An assistant that remembers you.** It keeps notes on your preferences and projects. You can read, pin or delete any of them.
- **Voice.** Talk to it and it talks back. Speech runs on your own machine.
- **Sharing.** Sync your apps to a GitHub repo and anyone can install them.
- **A robot.** A small robot lives on your desktop. It climbs your icons, chases bugs, answers questions, and can turn your desktop into a level you play.

## It asks first

By default the assistant asks before it changes anything. Deleting and publishing always ask, whatever the setting. It can only write to your own folders, it has no way to run commands on your computer, and every app it builds runs in a sandbox.

## Install

1. Download `one_OS-Setup-<version>.exe` from the [latest release](https://github.com/jvanlaar5930/OneOs-installer/releases/latest).
2. Run it. The installer isn't code-signed yet, so if Windows SmartScreen appears, click **More info**, then **Run anyway**.
3. Open one_OS and choose an AI in **Settings → AI Backend**.

You need Windows 10 or 11 (64-bit). To update, run a newer installer. Your apps and settings are kept.

## Choosing an AI

- **Claude CLI (recommended).** Sign in with your claude.ai account. You don't need an API key.
- **Local model.** one_OS downloads a model sized for your machine and runs it offline. You don't need an account.
- **OpenAI-compatible server.** Use OpenAI, LM Studio, Ollama or another compatible service.

---

<p align="center">
  <sub>Built with curiosity and a healthy disregard for how desktops are supposed to work.</sub>
</p>
