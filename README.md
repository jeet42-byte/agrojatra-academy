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

Six timed MCQ tests (ISSB IQ 39, GK 42, Math 38, English 36, Bangla 36, Cadet college 38 questions, 229 in all; each attempt draws a fresh set of 25; open one directly with tests.html#iq, #gk, #math, #eng, #bangla or #cadet), one minute per question, questions in a new random order on every attempt, with a score and an explanation for every answer at the end. Each visitor's best score is kept in their own browser.

To add or edit questions, change the `TESTS` list at the top of the script in `tests.html`. Each question is `["question", ["option 1", "option 2", "option 3", "option 4"], index of the correct option starting at 0, "explanation"]`.

## Brand files (`assets/`)

- `favicon.svg`: icon used in the browser tab and site header
- `mark.svg`: the chevron mark on its own (transparent background)
- `agrojatra-logo.png`: full logo for documents and posters (1200 × 400)
- `agrojatra-profile.png`: Facebook / WhatsApp profile picture (720 × 720)
- `agrojatra-cover.png`: Facebook cover photo (1640 × 624), also the preview image when the site link is shared

## Viva prep (`viva.html`)

Common viva questions for ISSB, soldier/Ansar and cadet college, each with a tip on how to answer, plus a WAT trainer that shows 20 random words for 15 seconds each, and 20 SCT sentence stems with sample answers. Edit the `WORDS` list in the script to change the words.

## 8-week ISSB plan (`issb-plan.html`)

Week-by-week plan for the officer cadet ISSB course, linked from the three ISSB course cards. Edit the weeks directly in the page.

## Recruitment guide (`recruit.html`)

For soldier, sailor, airman and Ansar-VDP candidates: links to the official recruitment sites, the usual selection steps, a document checklist, an 8-week fitness plan (our own training targets, not official standards) and a scam warning. Eligibility numbers change with every circular, so the page points to the official circular instead of listing exact figures.

## English home page (`en.html`)

English version of the home page (linked from the Bangla menu and footer). The detailed pages (tests, viva, ISSB plan, recruitment guide) are Bangla only. When you change fees, the routine or the batch date, update both `index.html` and `en.html`.

## Batch start banner

The red banner at the top of `index.html` and `en.html` shows the next batch date and a countdown. To change the date, edit the banner text and `BATCH_START` in the script of both pages. The banner hides itself after the start date.

## Free downloads (`downloads.html`, `assets/pdf/`)

Free study PDFs: ISSB complete guide, Bangladesh & defence GK sheet, math formula sheet, picture IQ, picture story, and a 229-question bank with answers and explanations (built from the questions in `tests.html`). To add a new PDF, put it in `assets/pdf/` and copy one of the `<article class="file">` cards in `downloads.html`.

## Picture IQ (`nonverbal.html`) and picture story (`ppdt.html`)

- `nonverbal.html`: 30 non-verbal IQ questions (rotation, series, odd one out, 3×3 matrix, mirror and water images, analogy). The figures are drawn as SVG in the `NONVERBAL` list in the page script; the first option of each question is the correct one and options are shuffled on screen.
- `ppdt.html`: 6 hazy practice scenes (SVG in the `PPDT` list) with a 30-second view / 4-minute write timer, points to notice and a sample story for each.
