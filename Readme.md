<p align="center">
  <img src="assets/orbit-logo.gif" alt="one_OS" width="400" />
</p>

<h1 align="center">One OS</h1>

<p align="center">
  <strong>A desktop operating system that builds its own apps.</strong><br/>
  <em>Describe what you want. Watch it appear.</em>
</p>

<p align="center">
  <a href="https://github.com/jvanlaar5930/OneOs-installer/releases/latest"><img src="https://img.shields.io/github/v/release/jvanlaar5930/OneOs-installer?style=for-the-badge&label=Download&color=8a6bff" alt="Download the latest release"/></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platform-Windows_10%2F11_x64-0f1118?style=flat-square" alt="Platform"/>
  <img src="https://img.shields.io/badge/Claude_CLI-ready-8a6bff?style=flat-square" alt="Claude CLI"/>
  <img src="https://img.shields.io/badge/local_models-built_in-22c55e?style=flat-square" alt="Local models"/>
  <img src="https://img.shields.io/badge/OpenAI--compatible-API-5b9bff?style=flat-square" alt="OpenAI compatible"/>
</p>

---

## 📥 Download and install

1. Open the **[latest release](https://github.com/jvanlaar5930/OneOs-installer/releases/latest)** and download `one_OS-Setup-<version>.exe`.
2. Run it. You choose where to install it, and you get a desktop and Start menu shortcut. It installs for your user only and does not need administrator rights.
3. Launch **one_OS**. On first launch it asks who you are and what to call your assistant. Then connect an AI, as described in [Connect an AI](#-connect-an-ai) below.

> **Windows SmartScreen:** the installer is not code-signed yet, so Windows may show *"Windows protected your PC"* the first time you run it. Click **More info → Run anyway**.

**Updating:** download the newer installer from [Releases](https://github.com/jvanlaar5930/OneOs-installer/releases) and run it over the top. Your apps, files, settings and memory are kept.

**Uninstalling:** Windows Settings → Apps → Installed apps → **one_OS** → Uninstall.

---

## ⚡ What is one_OS?

> **There are no pre-installed apps. The only thing waiting for you is an assistant that can build them.**

one_OS is a full desktop environment: wallpaper, window manager, taskbar, virtual file system and a Start menu. It is built on one premise: **apps don't ship with the OS. You ask for them.**

Talk to the assistant. Ask a question and it answers. Ask it to work on your files and it does. Ask for an app and it plans, writes and installs one: a real, running application on your desktop that you can edit. Ask it to change something and it rewrites the app. Every app you make is kept in your personal app library, which you can sync to GitHub and share with anyone.

There is **one agent and one conversation**. You never pick a mode. The assistant decides whether to answer, act on the OS, or hand the work to the coding agent or Game Studio.

```
  You      →  "Make me a kanban board with swimlanes"
  Agent    →  plans it, writes the code, installs it
  Desktop  →  app appears, runs, persists — yours forever

  You      →  "Summarise the notes in my Documents folder"
  Agent    →  reads them, answers — no build, no window, no mode switch

  You      →  "Remind me to stretch every 30 minutes"
  Agent    →  schedules it, and tells you it only runs while one_OS is open
```

### 🧪 Your PC is your sandbox

Build what you want, when you want it. There are no installs, no app stores and no permission slips. Have an idea at midnight? Build it. Want a tool that works exactly the way you think? Describe it. The OS adapts to you.

Every app you build is **yours**: stored locally, versioned, and editable at any time. Don't like how it looks? Tell the assistant. Need a new feature? Ask for it. Your apps change when you want them to, not when a developer ships an update. Every feature you ask for is recorded in the app's build plan, so if a build goes wrong, the assistant can regenerate the whole app from scratch.

### 🌐 Share what you build

one_OS apps are stored as plain files in a GitHub repository, so sharing an app means pushing a commit. Publish your app library and anyone can browse it, install from it and build on it. Find something you like in the community store? Pull it to your desktop in one click and make it your own.

There is no walled garden, no marketplace cut, and no account needed to share.

### 🔮 A desktop that thinks ahead

Traditional operating systems ship frozen. In one_OS the assistant is the foundation, not a feature added later. You can inspect, change and extend every part of the OS by asking for it in plain language. The more you use it, the more it fits you.

### 🧠 An assistant that remembers you

On first launch the OS asks who you are, what to call your assistant, and how you want it to work. It saves your answers to **`/Documents/USER.md`**, a plain markdown file you can open and edit like any other.

It also keeps a **long-term memory** of your preferences, decisions and projects. The memory has a size limit. Entries are ranked by how recently they were *used*, and when the memory fills up, the assistant merges old entries into fewer, more accurate ones instead of cutting them off. You can see everything it remembers in Settings, and pin or delete any entry.

It also **learns from its own work.** When a build fails or an app's self-tests fail, it writes down the lesson as a reusable skill. Those skills stay **drafts** until you activate them. It proposes; you decide.

### 🛡️ Guard rails, because it has real access

The assistant can use tools on your OS, so the permission model was built first and everything else was built behind it.

- **Deny by default.** Every tool call is checked before it runs. Anything unrecognised is refused.
- **Judged on actions, not on what it says.** Each decision is based only on the tool and its arguments, never on the model's description of what it is doing. A prompt hidden in a file or a generated app can't talk its way into more access.
- **Limited folders.** It writes only inside `/Documents`, `/Desktop`, `/Downloads`, `/Projects` and `/tmp`. `/System` and `/Apps` are refused even if you approve.
- **Deleting and publishing always ask you first**, at every autonomy level, with no exceptions and no "remember this choice".
- **Reading the web can be allowed for a session**, and nothing else can. One question is often a search plus several pages, and approving each page trains you to click through without reading. The session grant covers exactly two tools, is never saved to disk, never applies to a scheduled task, and can be revoked in Settings.
- **Some things are not possible at all.** It has no way to run shell commands, run arbitrary code, or change its own permissions.

You choose how much freedom it gets in **Settings → Assistant**:

| Level | What it means |
|---|---|
| **Ask before changing anything** | It reads freely and asks you to approve every change (default) |
| **Work independently on routine changes** | Routine writes happen without asking. Deleting and publishing still ask, every time |
| **Conversation only — no tools** | It talks and does nothing else. This also stops background learning and scheduled tasks |

### 🗣️ Two shells, one assistant

The desktop is one way to use the OS. Switch to the **assistant shell** (**Settings → Appearance → Shell**) and the window manager goes away. You get one full-screen conversation, an orb that shows what the assistant is doing, and apps that fill the screen when opened instead of floating in windows.

The assistant is the same in both shells: same agent, same tools, same guard rails, same conversation. If you switch mid-sentence, the conversation continues. `Ctrl+Shift+F` leaves a full-screen app. It is not `Esc`, because games need that key.

It **listens and speaks**, both on your machine:

- **Speech to text** uses a local Whisper model, or your AI provider if you prefer. A global hotkey turns on the microphone from anywhere in the OS.
- **Speech out** uses Kokoro, which runs inside one_OS itself, with no server and no API key. Download one model once and it speaks offline, in any of 28 voices. You can also use your system voices or any OpenAI-compatible speech endpoint.
- **It stops talking as soon as you start**, and can leave the microphone on after it answers so a spoken conversation keeps going.

Long conversations are handled the way a person handles them: older turns are summarised so recent ones fit, instead of the start of the conversation being dropped.

### ⏰ Work that happens without you

Ask for something to repeat and the assistant schedules it: a recurring check, a daily summary, or a reminder every ten seconds if you want. Tasks can also wait for an **event** instead of a time, such as an app hitting an error, so the OS can investigate its own failures.

Two things to know up front (the assistant will tell you too):

- **Tasks only run while one_OS is open.** Nothing runs while it's closed. Anything that came due is run once on the next launch.
- **A new task starts read-only.** It can look at anything but change nothing until you grant it permission in Settings. No task can ever delete anything or reach outside the OS, whatever you grant it.

### 🤖 Meet your robot friend

Your assistant has a body. A small robot lives on the desktop, using whatever name you gave your assistant (Tigtug by default). It walks along the bottom of the screen, blinks, says the odd line, and keeps you company while you work.

**Click it** and a ring of options appears:

- **Pet it, tickle it, feed it a battery, make it dance, spin it until it's dizzy, give it a zap, or put it down for a nap.** Each has its own animation, face and commentary.
- **Ask a Question** opens a speech bubble. The answer comes from the *same* assistant you talk to everywhere else, streamed live, with a button to continue in the full chat.
- **Drag it anywhere.** It dangles, kicks, and lands with a squash.

**It has a life of its own, too:**

- **It changes with its size** (**Settings → Robot**). At normal size it walks over to your icons, **climbs** up a column, looks around and **jumps off**. Make it big and it stomps across the desktop, **knocking icons aside**. They always spring back, so your layout is never changed.
- **It hunts bugs.** Every so often a tiny beetle runs onto the desktop. The robot chases it and squashes it with a hop and a pun: *"Bug fixed. No PR needed."* Click the bug first and the robot complains that you stole its catch.
- **It reacts to real work.** While Game Studio builds, a gear spins above its head. It dances when a scene is done and looks worried when one fails.
- **The assistant can control it.** Ask for a dance, a victory lap or a message delivered in person. Harmless actions run without asking. Resizing it changes a setting, so the assistant asks first, like any other change.

**It also has its own game.** Pick **Playground** from its menu and the desktop becomes a level editor with the robot as the hero:

- **Draw** platforms with your mouse (your desktop icons count as platforms too), then press an arrow key to **play**: run, jump and stomp.
- **Right-click to place** stars, coins, health hearts, coloured **key cards** and the **doors** they unlock, spikes, three kinds of **monsters**, a **boss** that guards the goal, and a finish flag.
- **Select any line** to make it a **moving platform** (you choose its direction, distance and speed) or a **crumbling** one that falls a few seconds after you land on it.
- **Build whole games.** Save them by name, then open, rename, duplicate or delete them later. Unfinished work is kept as a draft, so `Esc` returns the desktop to normal without losing anything.
- **Use it in Game Studio games too.** Game Studio can use your robot as a ready-made character in any game you ask for (*"a platformer starring Tigtug"*).

Don't want company? Turn it off in **Settings → Robot**.

---

## 🚀 Features

| | Feature | What it does |
|---|---|---|
| 💬 | **Personal assistant** | One agent, one conversation. It decides whether to answer, act on your files, or build. No mode picker |
| 🗣️ | **Assistant shell** | A full-screen conversation instead of the desktop. Same agent, same conversation, no windows |
| 🎙️ | **Voice in** | Local Whisper speech-to-text with a global hotkey, or your AI provider if you prefer |
| 🔊 | **Voice out** | Kokoro runs inside the OS: offline, no server, no API key, 28 voices. Speaks each sentence as it's written |
| 🌐 | **Web search and reading** | Searches and reads web pages to answer about news, weather, prices and docs. One approval covers a session |
| 🖥️ | **Local models** | Run a model on your own machine. one_OS downloads the engine and the model and picks settings that fit your hardware |
| 🔎 | **Settings search** | Find any setting by name instead of hunting through tabs |
| 👤 | **USER.md profile** | A first-run wizard saves who you are and how you like to work to a markdown file you can edit |
| 🧠 | **Long-term memory** | Has a size limit, ranks entries by recent use, and merges old entries instead of deleting them |
| 🛡️ | **Guard rails** | Every tool call is checked and refused by default, writes are limited to your folders, and each turn has limits |
| 🎚️ | **Autonomy levels** | Conversation only, ask first, or work independently. Deleting and publishing always ask |
| ⏰ | **Scheduled tasks** | Recurring work down to seconds, read-only until you grant more. Runs only while the OS is open |
| 🔔 | **Event triggers** | Tasks that run when an app errors or a build fails, with cooldowns so a crash loop can't flood you |
| 🎓 | **Self-taught skills** | Failed builds and failed self-tests become reusable lessons, saved as drafts you activate |
| 🤖 | **Desktop robot** | Your assistant with a body. Climbs icons, squashes bugs, answers questions, and reacts to Game Studio builds |
| 🕹️ | **Robot Playground** | Draw levels on your desktop and play them: moving and crumbling platforms, keys and doors, monsters, a boss, and saved games |
| 🤖 | **AI app builder** | Describe any app in plain language and the assistant plans, writes and installs it |
| 📋 | **Build checklists** | Large requests are split into a step-by-step build plan. If a step fails, retry just that step |
| 📝 | **Plans that grow** | Every change is added to the app's build plan, so it always reflects everything you've asked for |
| 🛟 | **Rewrite from Plan** | Regenerate an app from its plan in one click, to recover from a bad build |
| ✅ | **Self-tests** | Every app comes with its own tests, and a broken build is stopped before it opens |
| 🧩 | **Finalize** | Large apps can be written as real components and compiled into a runnable app when you're ready |
| ⚙️ | **App Settings panel** | View an app's plan, Finalize, Rewrite from Plan, and re-sync to GitHub, all in one place |
| ✨ | **Quick-action chips** | One click to polish an app, add dark mode, make it responsive, improve accessibility, or review it for bugs |
| 🪟 | **Window manager** | Drag, resize, minimize, maximize, fullscreen and stack windows, like any desktop |
| 🗂️ | **File system** | `/Desktop`, `/Documents`, `/Apps` and more, saved between sessions |
| 🔒 | **Sandboxed apps** | Every generated app runs isolated from the OS and can only reach it through a permission-checked bridge |
| 🔑 | **App permissions** | Apps ask for permissions before they load. Grant, deny or reset them per app in Settings |
| 🗄️ | **Per-app database** | Apps can keep their own private database, offline by default |
| 🌐 | **Permissioned network** | Apps can reach the network only with permission, through the OS |
| 💬 | **App-to-app messaging** | Running apps can send each other data |
| 🔁 | **App iteration** | Chat with the assistant to change any app in place, with a full build history per app |
| 🎮 | **Game Studio — 3D** | An AI game builder for 3D games: multiple scenes, a live canvas, materials, audio, NPCs and quests, and publish-to-app |
| 🕹️ | **Game Studio — 2D** | The same workflow for 2D games: platformers, top-down and puzzle games |
| 🔁 | **Auto-fix** | After every build, a review step checks the code and fixes problems before the build is marked complete |
| 🐛 | **Bug review** | A quick-action chip reviews an app or game, fixes what it finds, and checks it against the original plan |
| ✨ | **AI-generated icons** | After each build the assistant offers three custom icons. Pick one or keep the default |
| 🔔 | **Notifications** | Apps can show notifications inside the one_OS desktop |
| 🕹️ | **Game controls** | Pointer lock, gamepads and file export work inside apps |
| 🐙 | **GitHub sync** | Push and pull your whole app library to a GitHub repository |
| 🔑 | **Claude CLI support** | Use your claude.ai Pro account, with no API key to manage |
| 🔀 | **Fallback model** | Pair Claude CLI with a local model. When Claude hits a usage limit, builds switch to the local model instead of stopping |
| 🎁 | **Starter apps** | Calculator, Calendar, Notes, Paint, Clock and Trash, all editable from day one |

---

## 🧠 Connect an AI

one_OS needs an AI to think with. Open **Settings → AI Backend** and choose one.

### Claude CLI (recommended)

> Use your **claude.ai Pro account**. There is no API key and no billing setup.

Select **Claude CLI** and click **Check status**. If the CLI isn't installed yet, the panel shows the install steps. Once it shows you as signed in, pick a model:

| Model | Best for |
|---|---|
| **Default** (Sonnet) | Balanced, efficient for routine work |
| **Opus** | Complex apps and harder reasoning, with higher usage than Sonnet |
| **Haiku** | Quick edits and light tasks |

### Local model (runs on your machine)

No account and no server of your own. Open **Settings → Local Models** and choose a model. one_OS downloads the engine and the model, picks settings that fit your machine's memory, and runs it alongside itself. Then select **Local model** in **Settings → AI Backend**.

The catalogue runs from small models (about 3 GB) for laptops to large models (about 16–22 GB) for machines with a strong graphics card. one_OS recommends one that fits your machine. If you already have models from LM Studio or llama.cpp, it can use them without downloading them again.

### Claude CLI + a local model as a fallback

Use Claude CLI and also set a local **worker model**, and one_OS keeps building through a usage limit. While Claude is available it does all the work. When Claude reports a usage limit, work moves to the local model until the limit resets.

### Other OpenAI-compatible providers

Choose **OpenAI-compatible server** and enter a Base URL, API key and model. This works with OpenAI, LM Studio (`http://localhost:1234/v1`), Ollama (`http://localhost:11434/v1`) and other compatible services.

---

## 🔊 Give it a voice

Speech is set up separately from your chat model.

**Talking to it.** Open **Settings → Voice Input**. Local Whisper is included: pick a model size and it downloads once. `Ctrl+Shift+M` turns on the microphone from anywhere in the OS, including inside a running app.

**Hearing it back.** Open **Settings → Text-to-Speech** and choose the **Built in** engine. Kokoro runs inside one_OS itself, with nothing to start or configure. Download one model and it works offline.

| Model | Size | Speed |
|---|---|---|
| **Standard** (default) | 163 MB | ~3.5× real time |
| **Compact** | 92 MB | ~1.2× real time |

Both run on the CPU. All 28 voices come with the OS, so you can choose a voice before downloading anything.

You can also use your system voices or any OpenAI-compatible speech endpoint. LM Studio does not provide one.

---

<p align="center">
  <sub>Built with curiosity and a healthy disregard for how desktops are supposed to work.</sub>
</p>
