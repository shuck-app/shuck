# Shuck privacy

**Effective 6 October 2026. Applies to Shuck Free 1.0 for Windows.**

Short version: Shuck reads your screen on your computer and keeps what it reads on your computer. There's no account, no analytics and no telemetry. Shuck goes online only to ask GitHub once a day whether there's a newer version (you can turn this off), and when you press **Join the waitlist**.

Shuck is made by Ansh Srivastava, an individual based in India. For this policy he is the person responsible for the limited information described below ("we", "us"). Contact: shuck.privacy@gmail.com. We reply within 30 days.

## What happens when you capture

When you press the shortcut, Shuck takes a picture of your screens and shows it frozen so you can drag a box. Everything after that happens on your computer:

- The picture stays in memory. Shuck doesn't save the full screen anywhere, and it's gone once the capture is done or cancelled.
- The part you selected is read by a text engine built into the app. Nothing is uploaded to read it.
- Shuck looks for links, email addresses and QR or barcodes, also on your computer.
- The text goes to your clipboard. Shuck only writes to the clipboard, it never reads what you copied elsewhere. If you've turned on **Clipboard history** or **Sync across devices** in Windows, Windows keeps a copy of what Shuck copies, just like anything else you copy.

## What Shuck stores, and where

Shuck keeps its files in your Windows user account: your user folder and your part of the registry, listed below. Shuck doesn't store anything on a server. Windows itself may keep copies of things you copy (see above).

| What | Where | What's in it |
|---|---|---|
| Library | `%APPDATA%\app.shuck.desktop\library.db` | Your last 20 captures: the text, the links and addresses found in it, what kind it was (text, link, QR…), the time, a search index of the text, and a small thumbnail of the captured area (at most 160 × 120 pixels). |
| Settings | `%APPDATA%\app.shuck.desktop\settings.json` | Your choices (shortcut, line breaks, text size and so on), window sizes, the date you joined the waitlist if you did, when Shuck last checked for updates, the newest version it saw and whether you dismissed its notice, and simple usage counts (see below). |
| Log | `%LOCALAPPDATA%\app.shuck.desktop\logs\shuck.log` | Technical notes for fixing bugs: timings, image sizes, character counts, errors. Shuck is built not to write the text you captured into the log. Error notes can include folder paths, which contain your Windows user name. |
| App window data | `%LOCALAPPDATA%\app.shuck.desktop\` | Working files of the Microsoft WebView2 component that draws Shuck's windows. |
| Launch at login | Windows registry, `HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run`, value `Shuck` | Launch at login is on by default. You can turn it off during setup or in **Settings → General**, which removes this value. The uninstaller removes it too. |
| Uninstall entry | Windows registry, under `HKEY_CURRENT_USER` | The entry Windows uses to list Shuck in your installed apps. The uninstaller removes it. |

**Usage counts.** Settings keeps a few numbers, such as how many captures you've made, how many found no text, and how often you used each kind of button. They're counts only: never the text, links, addresses or anything you captured. They never leave your computer on their own. They're only included in the diagnostics that **Copy diagnostics** and **Report a problem** put on your clipboard, so you can read them and decide whether to paste them into a bug report.

**You're in control of the Library.** In **Settings → Library & privacy** you can:

- **Pause Library**: captures are still copied, but nothing is saved until you resume.
- Turn off **Save thumbnails**, or turn off **Save to Library** completely.
- Delete a single capture, or **Clear Library**. Both can be undone while the Undo button shows; after that they're deleted from Shuck. As with most apps, traces may stay recoverable on disk until Windows reuses the space. The Library file also reuses the space a deleted capture took instead of wiping it immediately. If you want every trace gone, use **Delete all data** (below).

## When Shuck goes online

Shuck goes online in two cases: the update check, which goes to GitHub, and **Join the waitlist**, which comes to us. It has no analytics. The only thing in Shuck that sends data to us is **Join the waitlist**.

**Checking for updates.** Once a day, and when you press **Check now** in **Settings → About**, Shuck asks GitHub whether there's a newer version. This is one HTTPS request to GitHub's public API (`api.github.com`) for the latest release of the Shuck repository. The request includes a User-Agent header with Shuck's name and version (for example `Shuck/1.0.0`) and a header naming the format of the answer. Shuck adds no ID, no account, no device or Windows details and no cookies. From the answer Shuck uses only the version number. It keeps, on your computer, the time it last checked and the newest version it saw.

Like any visit to a website, GitHub receives your IP address along with the request, and handles them under [GitHub's privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement). GitHub is based in the United States, so your request may be handled in a different country from yours. We don't receive the request ourselves.

Update checks are on by default. To turn them off, go to **Settings → General** and turn off **Check for updates**; while it's off, Shuck doesn't make this request. When a newer version is out, Shuck says so in its main window, in **Settings → About** and in the tray menu. It doesn't download or install anything itself: **Get it** opens the releases page in your browser.

**Join the waitlist.** When you press **Join the waitlist** in Shuck's main window (Home), in **Settings → About**, or on the "another language" notice, Shuck sends one request to our counter (`shuck-waitlist.shuck-app.workers.dev`). The request contains only where you pressed the button: `{"surface":"home"}`, `"about"` or `"toast"`. No ID, no app version, no device details, no cookies. Shuck sends it once, doesn't retry, and remembers on your computer that you joined, so it doesn't count you again from the same install (unless you delete Shuck's data).

This is an anonymous count that shows how much interest there is. It doesn't sign you up for anything, and we have no way to contact you about it. To hear about Pro, watch the repository's releases on GitHub.

Our counter keeps one number per day for each of those three places (and one for requests it can't read). That's all. We don't store, log or look at your IP address, and we have switched off logging in our counter.

To deliver the request, the counter runs on Cloudflare, which works for us as our hosting provider. Cloudflare's network necessarily receives your IP address to carry the request, and Cloudflare keeps its own short-term security records, as described in [Cloudflare's privacy policy](https://www.cloudflare.com/privacypolicy/). Cloudflare runs servers worldwide, so your request is handled by a server near you, which may be in a different country from yours. Cloudflare uses recognised safeguards for such transfers; see its policy for details.

Pressing the button is your choice. If you don't press it, nothing is sent.

**Links you choose to open.** Buttons like **Open link**, **Email**, **Report a problem**, **What should Pro do?**, **Privacy**, **Get it** and **Get the latest version** open a page in your web browser. From then on it's your browser talking to that website (for our pages, that's GitHub), under that website's privacy policy. Shuck itself sends nothing. Choosing Gmail or Outlook.com for **Email** opens a new message with the address filled in; nothing is sent until you press Send there.

**Installing.** The installer comes from GitHub. If the Microsoft WebView2 Runtime is missing (Windows 11 already has it), the installer downloads it from Microsoft. Windows SmartScreen or Microsoft Defender may also check the downloaded installer with Microsoft.

**Microsoft components.** Shuck draws its windows with Microsoft WebView2. Its windows are pages inside the app and need no internet, so Shuck asks WebView2 not to make requests of its own, such as looking up your Windows account or downloading its configuration and components. Microsoft's Edge updater still keeps the WebView2 Runtime itself up to date for every app that uses it, and what Windows sends to Microsoft depends on your Windows privacy and diagnostic settings, not on Shuck. "No telemetry" in this policy means Shuck's own code.

**Uninstalling.** The uninstaller's last page has a **Tell us why you uninstalled** box, unticked by default. Only if you tick it, the uninstaller opens our "Uninstalled? Tell us why" discussion page on GitHub in your browser. The page address includes your Shuck version and `os=win`. GitHub receives that like any page visit; we don't receive anything ourselves. Answering is optional, needs a GitHub account, and your answer is public.

## What Shuck doesn't do

- No accounts and no sign-in.
- No analytics, telemetry, crash reporting or ads.
- No selling or sharing of data. We don't have your data to share.
- Shuck doesn't upload your screen, your captures or your clipboard.

## Deleting your data

- **In the app:** Settings → Library & privacy → **Delete all data**. This removes your Library, settings and log. You can undo it while the Undo button shows; after that the files are deleted. Launch at login stays as you set it.
- **When uninstalling:** tick **Also delete my captures and settings**. This removes both Shuck folders listed above.
- **By hand:** quit Shuck from the tray, then delete these two folders:
  - `%APPDATA%\app.shuck.desktop`
  - `%LOCALAPPDATA%\app.shuck.desktop`

  Paste each path into the File Explorer address bar to find it.
- **The waitlist count** can't be deleted per person, because nothing in it points to you.

## Your rights

We don't hold information that identifies you, so there's usually nothing for us to look up, correct or delete. Everything Shuck stores is on your computer, and you can see and delete it yourself (see above). Depending on where you live (for example the EU, UK, India or California) you may have rights to ask what we hold, to have it corrected or erased, to object, and to complain. To use any of them, or to raise a concern, email shuck.privacy@gmail.com. If you're not satisfied, you can complain to your local data protection authority.

We don't sell or share personal information, and we don't use it for advertising or profiling.

The only request that reaches us is the waitlist count, and the basis for it is your choice to press the button. It can't be withdrawn per person because nothing links the count to you. If you don't want to be counted, don't press the button. The update check goes to GitHub, not to us, and you can turn it off in **Settings → General**.

## Children

Shuck isn't aimed at children and has no accounts, so it doesn't know anyone's age. It doesn't track, profile or advertise to anyone, including children. The one waitlist request contains no personal information. If you believe a child's information has reached us, email shuck.privacy@gmail.com and we'll look into it.

## Changes

If this policy changes, the new version will be in this file with a new effective date, and the change will be listed in the release notes. Past versions are in this file's history on GitHub. If a future version of Shuck sends more information than described here, we'll say so here before that version is released. Each version of Shuck is covered by the policy in force when it was released, unless a newer policy says otherwise.

## Questions and privacy requests

Email shuck.privacy@gmail.com for any privacy question, request or complaint. It's a private inbox, so it's the right place for anything personal. For general questions you can also open an [issue](https://github.com/shuck-app/shuck/issues/new/choose) or ask in [Discussions](https://github.com/shuck-app/shuck/discussions). Both are public, so please don't include personal details or captured text there.
