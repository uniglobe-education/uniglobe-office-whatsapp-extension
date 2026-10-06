# UniGlobe Office WhatsApp

The Chrome extension for UniGlobe counselors' **registered office WhatsApp numbers**. It connects WhatsApp Web to the UniGlobe CRM so eligible direct chats and counselor replies stay with the same student record. Downloading this public ZIP does **not** grant CRM access; an admin must assign your office number to your own CRM account.

[Download the extension ZIP](https://raw.githubusercontent.com/uniglobe-education/uniglobe-office-whatsapp-extension/main/uniglobe-office-whatsapp.zip)

## Setup guide for counselors

Use Google Chrome on your work computer. Keep your office phone nearby. If you share a computer, create a separate Chrome profile for yourself (profile icon at the top right → **Add**). Do not connect a personal or another counselor's WhatsApp account.

1. Download the ZIP above and **extract** it to a folder you will keep, such as `C:\UniGlobe\office-whatsapp`. Do not move or delete that folder after installation.
2. In the **same Chrome profile** you use for the CRM, open `chrome://extensions`, turn on **Developer mode**, and click **Load unpacked**. Select the extracted folder containing `manifest.json`—not the ZIP file.
3. Confirm Chrome shows **UniGlobe Office WhatsApp**. Pin it from Chrome's Extensions (puzzle-piece) menu if you want its status one click away.
4. Sign in at [UniGlobe CRM](https://crm.uniglobeeducation.co.uk). If you have an assigned office number, the CRM checks the extension and guides you through any missing step. Read the privacy notice and choose **I understand and connect**.
5. The CRM pairs the extension to **your** account automatically. It opens or reuses a WhatsApp Web tab if needed. If you see a QR code, on your **office phone** open WhatsApp → **Linked devices** → **Link a device**, then scan the QR code.
6. Return to the CRM. The top-right **Office WhatsApp** badge must say **Connected**. If it says **Set up**, **Link WhatsApp**, **Wrong number**, or **Offline**, click it and follow the displayed instructions. An open WhatsApp tab alone does not prove syncing.

Only the office number assigned to your CRM account can pair. If the CRM says **No office number assigned**, ask your admin; do not try a different number. On first connection, syncing starts from the office account's enrollment time; old personal or office history is not imported automatically.

## Daily use

- Keep Chrome and one WhatsApp Web tab open during your shift. The CRM can be in another tab. Closing Chrome or letting the PC sleep pauses live sync; it catches up with messages WhatsApp Web still has when you return.
- New direct messages to your office number can create a CRM contact owned by you. Open **My Conversations** or **My Students** to work with them.
- To reply from the CRM, open the conversation and choose your **office WhatsApp** number under **Send from**. You may also reply in WhatsApp Web; eligible direct messages sync to the same CRM conversation.
- With the updated CRM, choose your office number and press **Call** to start an office voice call. The CRM shows call progress and **End call**; keep WhatsApp Web open for audio and allow its microphone prompt. Calls are not recorded.
- The UniGlobe panel at the right of WhatsApp Web shows the linked student and quick CRM actions. It can be collapsed with the **UniGlobe** tab.
- If a direct contact is a teammate, job seeker, or other non-student, use the conversation's **Mark as non-lead** control. That removes an office-only contact from student lists and counts while retaining its chat for audit. Do not classify an actual student this way.
- At the end of your shift, **log out of the CRM**. This signs the extension out of that CRM account. Closing only the CRM tab does not sign it out.

## If it does not connect

| CRM badge or popup | What to do |
| --- | --- |
| **Set up / extension not detected** | Check this Chrome profile at `chrome://extensions`; enable the extension, then click **Check again** in the CRM. |
| **Update needed** | Download the latest ZIP, extract it into your existing extension folder, then click **Reload** on its `chrome://extensions` card. Unpacked extensions do not auto-update. |
| **Link WhatsApp** | Scan the WhatsApp Web QR code with your registered **office** phone. |
| **Wrong number** | Sync and sending are paused. Log out of WhatsApp Web and link the correct office number; use separate Chrome profiles for separate counselors. |
| **Offline / syncing** | Keep Chrome and WhatsApp Web open. Click **Check again**; if it stays offline, check internet access or tell your admin. |
| **Signed out** | Sign back in to the CRM and reconnect. |

For a persistent problem, open the extension popup and click **Export diagnostics**, then send that file to your UniGlobe admin. It excludes message text.

## Scope and privacy

Only eligible one-to-one office chats sync. Groups, status updates, broadcasts, channels, calls, and view-once media are not captured. Do not use this extension with a personal WhatsApp number. Read the [CRM privacy policy](https://crm.uniglobeeducation.co.uk/privacy-policy) before connecting.

This is an internal UniGlobe tool, not an official WhatsApp or Meta product. It depends on WhatsApp Web being available and may need an update if WhatsApp Web changes.


## Version 1.0.13 — 6 October 2026

Files from your office WhatsApp reach the CRM reliably. Photos, PDFs and voice
notes copy in bigger pieces, files WhatsApp Web had not loaded yet are fetched
again automatically, and a file that still can't be copied shows "failed" with
a **Retry** button in the CRM instead of "syncing" forever. Includes everything
in 1.0.12. Works with CRM 0.1.36. Update the unpacked extension using the steps
above.

## Version 1.0.12 — 4 October 2026

Every call on your office WhatsApp now appears in the student's chat in the
CRM — incoming, outgoing and missed, whether you called from the CRM or from
your phone — with how long it lasted. Includes everything in 1.0.11. Works with
CRM 0.1.34. Update the unpacked extension using the steps above.

## Version 1.0.11 — 4 October 2026

Keeps WhatsApp Web connected when you are not looking at it. The extension
stops Chrome from putting the WhatsApp tab to sleep, and if the browser puts it
to sleep anyway (Edge "Sleeping tabs"), it wakes it up so it reconnects by
itself. Includes everything in 1.0.10. Works with CRM 0.1.33. Update the
unpacked extension using the steps above.

## Version 1.0.10 — 3 October 2026

Incoming calls on your office WhatsApp now ring in the CRM, with Answer and
Decline (the conversation itself stays in WhatsApp Web — keep that tab open and
allow the microphone). Missed calls are recorded on the student. Calls from the
CRM go out from your office number. Includes everything in 1.0.9. Works with
CRM 0.1.31. Update the unpacked extension using the steps above.

## Version 1.0.9 — 3 October 2026

Much faster sync. The extension now keeps its own local database of synced
messages, imports older chats three at a time without re-sending what it
already sent, and uploads files on their own track (three at a time). All
older text is imported; files from the last 6 months (older files show as
"not imported" in the CRM). Messages are no longer lost while Chrome wakes the
extension. Needs one new permission, "unlimited storage" (no warning). Includes
everything in 1.0.8. Works with CRM 0.1.29. Update the unpacked extension
using the steps above; once the Chrome Web Store version is approved, the CRM
offers a one-click switch to a version that updates itself.

## Version 1.0.8 — 3 October 2026

Fixes the office WhatsApp showing "offline" on and off while it was working.
After Chrome restarts the extension in the background, it now waits for the
WhatsApp tab before reporting, and a WhatsApp tab that was open before an
update is reloaded once so it reconnects by itself. Includes everything in
1.0.7 (calls, Not a student). Works with CRM 0.1.27. Update the unpacked
extension using the steps above; it does not auto-update.

## Version 1.0.7 — 3 October 2026

Everything in 1.0.6 (office call controls) plus a **Not a student?** card in the
sidebar: mark a chat as Teammate, Partner or Other and it is hidden from the CRM
and never counted as a student. When the same number chats with other staff
office numbers, the card says so, and shows a one-click "Yes" when a colleague
already marked it. Works with CRM 0.1.26. Update the unpacked extension using
the steps above; it does not auto-update.

## Version 1.0.6 — 3 October 2026

Adds office call controls for the updated CRM, with the call and End control
bound to the original WhatsApp tab. A timeout never automatically redials.
Repairs chat opening for the current WhatsApp Web build, including phone-number
to LID chat migration. The live adapter was tested with a designated contact:
the call connected and End ended it after 16 seconds. Full CRM calling requires
the corresponding CRM release. Update the unpacked extension using the steps
above; it does not auto-update.
