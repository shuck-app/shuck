<p align="center">
  <img src="docs/logo.svg" width="96" alt="Shuck logo">
</p>

<h1 align="center">Shuck</h1>

<h3 align="center">Pixels in. Text out.</h3>

<p align="center"><b>Copy text from anything on your screen.</b><br>
Free for Windows. Works offline.</p>

<p align="center">
  <a href="https://github.com/shuck-app/shuck/releases/latest"><b>Download for Windows</b></a>
</p>

<p align="center">
  <a href="#install">Install</a> ·
  <a href="https://github.com/shuck-app/shuck/issues/new/choose">Report a problem</a> ·
  <a href="https://github.com/shuck-app/shuck/discussions">Ideas</a> ·
  <a href="PRIVACY.md">Privacy</a> ·
  <a href="LICENSE.md">Licence</a>
</p>

![Shuck copying text from a paused video](docs/hero.gif)

Some text on your screen can't be selected, like video subtitles, screenshots, error messages and scanned PDFs. Shuck lets you copy it.

## How it works

1. Press <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>2</kbd>. Your screen freezes, even a playing video.
2. Drag a box around the text.
3. It's already copied. Paste it anywhere.

Shuck reads the text on your PC. It works offline. You don't need an account, and Shuck doesn't upload your captures.

## What else it does

| Feature | What it does |
|---|---|
| **Links and emails** | Gives you a button to open the link or write the email. |
| **QR codes and barcodes** | Reads them too. |
| **Library** | Keeps your last 20 captures. Search them and copy them again. |
| **Line breaks** | Keep them as they are, or join lines into paragraphs. |
| **Your own shortcut** | Pick your own keys with Ctrl or Alt. |
| **Tray app** | Starts with Windows. You can turn this off. |
| **Accessibility** | Works with the keyboard and screen readers. Text size goes up to 225%. |

<p align="center">
  <img src="docs/toast.png" width="32%" alt="The notification after a capture, with Open link and Email">
  <img src="docs/home.png" width="32%" alt="Shuck's main window">
  <img src="docs/library.png" width="32%" alt="The Library">
</p>

**Good to know**

- Shuck reads English for now.
- Tables paste as plain text, one row per line.

## Install

1. **[Download the latest version](https://github.com/shuck-app/shuck/releases/latest).**
2. Run the file you downloaded. Its name looks like `Shuck_x.y.z_x64-setup.exe`.
3. That's it. You don't need admin rights.

<details>
<summary><b>Seeing "Windows protected your PC"?</b></summary>

Shuck isn't code-signed yet. Signing costs money, and Shuck is free. So Windows shows a warning the first time.

1. Click **More info**.
2. Check that the file name starts with `Shuck_` and that you got it from the download link above.
3. Click **Run anyway**.

![SmartScreen: click More info](docs/smartscreen-1.png)
![SmartScreen: Run anyway](docs/smartscreen-2.png)

</details>

**You need:** Windows 10 or 11 (64-bit) and about 20 MB of space. Shuck also needs Microsoft WebView2. Windows 11 already has it. If your PC doesn't, the installer gets it from Microsoft.

**Updates:** Shuck checks GitHub once a day for a new version and tells you. You can turn this off in Settings. To update, run the new installer. Your captures and settings stay.

**Uninstall:** Open Windows Settings, then Apps. Find Shuck and click **Uninstall**. To remove your captures and settings too, tick **Also delete my captures and settings**.

## Shuck Pro is coming

Here's what we're planning:

- Tables that paste as cells
- Code that keeps its indentation
- More languages
- A Library with no limit

Tell us what you want in **[What should Pro do?](https://github.com/shuck-app/shuck/discussions/categories/what-should-pro-do)**

In Shuck, you can press **Join the waitlist**. It adds one anonymous count, so we know how many people want Pro. It doesn't sign you up for anything. To hear when Pro is out, watch this repo's releases.

## Need help?

- **Something broke?** [Report a problem](https://github.com/shuck-app/shuck/issues/new/choose). In Shuck, go to **Settings → About → Report a problem**. It copies some details for you to paste. They're built to leave out your captured text and images.
- **Have an idea or a question?** Ask in [Discussions](https://github.com/shuck-app/shuck/discussions).
- **Uninstalled Shuck?** [Tell us why](https://github.com/shuck-app/shuck/discussions/categories/uninstalled-tell-us-why).
- **Found a security issue?** [Report it privately](https://github.com/shuck-app/shuck/security/advisories/new).

Issues and Discussions are public. Please don't post captured text or screenshots of your screen.

## Privacy

- Shuck doesn't upload your captures.
- No account, no analytics, no telemetry.
- Shuck itself goes online in two cases:
  - The daily update check. You can turn it off.
  - When you press **Join the waitlist**. It sends one word: where you pressed it.

Read the full version in **[PRIVACY.md](PRIVACY.md)**. Private questions: shuck.privacy@gmail.com.

## Licence

- Free to use, at home or at work.
- Not open source. © 2026 Ansh Srivastava, all rights reserved.
- Please don't sell it, share changed copies, or reverse engineer it.
- To share Shuck, share a link to this page, not the installer file.

Full terms are in **[LICENSE.md](LICENSE.md)**. Open-source parts keep their own licences. See them in **Settings → About → Open-source licences**.

This repo has releases, docs and feedback. The source code is private.

Made by Ansh Srivastava ([@xblackwaterx](https://github.com/xblackwaterx)).
