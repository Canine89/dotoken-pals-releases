# Dotoken Pals

![Dotoken Pals](images/cover.png)

A tiny pixel pet that lives at the bottom of your Mac screen and keeps an eye on your **Claude Code** and **Codex** sessions and weekly usage.

**[⬇ Download for Mac (free)](https://github.com/Canine89/dotoken-pals-releases/releases/latest/download/DotokenPals.dmg)** · **[Get Pro ($7.99)](https://gumroad.com)** · macOS 13+ · Apple Silicon & Intel

## What it does

- **Click the pet** to see every running Claude Code / Codex session and how much weekly usage is left.
- **One bird per session.** It flies in when a session starts and away when it ends. It pecks while working, hops with a `!` when it needs your input, and dozes when idle.
- A speech bubble shows your remaining weekly usage every so often.
- English, 한국어, 日本語, 简体中文 · light & dark.
- Everything is read locally. Nothing leaves your Mac.

![Session pals](images/birds.png)

![Panel](images/panel.png)

## Free vs Pro

| | Free | Pro |
|---|---|---|
| Sessions, usage panel, speech bubbles, fence | ✓ | ✓ |
| Pets | cat, dog, chick | + rabbit, hamster, fox, panda, pig, penguin, frog, capybara, ghost |
| Session pal themes | birds | + fireflies, ghosts |
| Choose your pet's personality | | ✓ |

![Pets](images/lineup.png)

![Themes](images/themes.png)

Pro is a one-time purchase for 2 Macs, with free updates. Activate it from the menu bar: **Activate Pro…**

## Install

1. Download **DotokenPals.dmg** and open it.
2. Drag **Dotoken Pals** into **Applications**, then open it.
3. For Claude Code's weekly usage, do the one-minute setup below.

The app updates itself when a new version is out.

### Claude Code usage setup (1 minute)

Sessions and Codex usage work right after installing. **Claude Code's weekly usage** needs a one-time setup: it connects the limit info Claude Code passes to its statusline so the app can read it.

Open `~/.claude/settings.json` and follow whichever case applies to you.

**If you don't use a custom statusline**, add this:

```json
{
  "statusLine": {
    "type": "command",
    "command": "sh /Applications/DotokenPals.app/Contents/Resources/claude-statusline-hook.sh"
  }
}
```

**If you already have a statusline**, put the hook **in front of** your existing `command`. Your statusline keeps looking the same.

```json
"command": "sh /Applications/DotokenPals.app/Contents/Resources/claude-statusline-hook.sh bash ~/.claude/statusline-command.sh"
```

Replace `bash ~/.claude/statusline-command.sh` in the example with the command you were already using.

Save, then send one message in Claude Code. Your weekly usage appears in the panel and updates automatically every time Claude Code responds.

> Limit info is provided when you sign in to Claude Code with a Claude subscription. It may not appear if you use an API key.


---

이 저장소는 Dotoken Pals 배포 파일만 올리는 곳입니다. 앱은 무료로 받고, Pro는 Gumroad에서 살 수 있습니다.

Claude is a trademark of Anthropic, PBC. Codex is a trademark of OpenAI. Dotoken Pals is an independent app, not affiliated with either company.
© 2026 Hyun Gyu Park.
