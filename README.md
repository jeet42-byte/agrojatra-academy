# Agrojatra Academy (অগ্রযাত্রা একাডেমি)

Landing and course page for an online coaching academy covering:

- ISSB for Bangladesh Army, Navy and Air Force officer cadets (preliminary written, viva, ISSB)
- Soldier / sailor / airman recruitment (written + viva)
- Ansar-VDP recruitment (written + viva)
- Cadet college admission (class 7)

It's one static file (`index.html`) with no build step.

## Before going live, edit these

| What | Where in `index.html` |
| --- | --- |
| Academy name (set: Agrojatra Academy) | `<title>`, `.brand`, footer |
| WhatsApp number for the enrol form (set) | `var WHATSAPP = "8801846877898"` in the script at the bottom |
| Number shown for WhatsApp / bKash / Nagad (set) | `<span id="phone">` |
| Course fees (set: ISSB ৳2,500 launch offer, regular ৳3,500; soldier ৳1,200; Ansar ৳800; cadet college ৳1,500/month; model tests ৳300) | each `.price` in the Courses section, and the `.offer` line above the cards |
| Subjects per course | the `<ul>` in each course card, check against the latest official circular |
| Class times | FAQ "ক্লাস কখন হয়?" |

## How enrolment works

The form doesn't need a server. When a student submits it, the page opens WhatsApp with their name, phone, course and district already typed in. They pay by bKash/Nagad Send Money and send you the transaction ID.

## Hosting (free)

- **GitHub Pages:** push this repo, then Settings → Pages → Deploy from branch `main`, folder `/`.
- **Netlify:** drag the folder onto app.netlify.com/drop.

## Free model tests (`tests.html`)

Five timed MCQ tests (ISSB IQ 27, GK 28, Math 24, English 24, Bangla 24 questions), one minute per question, questions in a new random order on every attempt, with a score and an explanation for every answer at the end. Each visitor's best score is kept in their own browser.

To add or edit questions, change the `TESTS` list at the top of the script in `tests.html`. Each question is `["question", ["option 1", "option 2", "option 3", "option 4"], index of the correct option starting at 0, "explanation"]`.

## Brand files (`assets/`)

- `favicon.svg`: icon used in the browser tab and site header
- `mark.svg`: the chevron mark on its own (transparent background)
- `agrojatra-logo.png`: full logo for documents and posters (1200 × 400)
- `agrojatra-profile.png`: Facebook / WhatsApp profile picture (720 × 720)
- `agrojatra-cover.png`: Facebook cover photo (1640 × 624), also the preview image when the site link is shared

## Viva prep (`viva.html`)

Common viva questions for ISSB, soldier/Ansar and cadet college, each with a tip on how to answer, plus a WAT trainer that shows 20 random words for 15 seconds each. Edit the `WORDS` list in the script to change the words.
