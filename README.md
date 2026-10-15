# Shapath Defence Coaching (শপথ ডিফেন্স কোচিং)

Landing and course page for an online coaching academy covering:

- ISSB for Bangladesh Army, Navy and Air Force officer cadets (preliminary written, viva, ISSB)
- Soldier / sailor / airman recruitment (written + viva)
- Ansar-VDP recruitment (written + viva)
- Cadet college admission (class 7)

It's one static file (`index.html`) with no build step.

## Before going live, edit these

| What | Where in `index.html` |
| --- | --- |
| Academy name | `<title>`, `.brand`, footer |
| WhatsApp number for the enrol form | `var WHATSAPP = "8801XXXXXXXXX"` in the script at the bottom |
| Number shown for WhatsApp / bKash / Nagad | `<span id="phone">` |
| Course fees | each `.price` in the Courses section (current values are placeholders) |
| Subjects per course | the `<ul>` in each course card, check against the latest official circular |
| Class times | FAQ "ক্লাস কখন হয়?" |

## How enrolment works

The form doesn't need a server. When a student submits it, the page opens WhatsApp with their name, phone, course and district already typed in. They pay by bKash/Nagad Send Money and send you the transaction ID.

## Hosting (free)

- **GitHub Pages:** push this repo, then Settings → Pages → Deploy from branch `main`, folder `/`.
- **Netlify:** drag the folder onto app.netlify.com/drop.
