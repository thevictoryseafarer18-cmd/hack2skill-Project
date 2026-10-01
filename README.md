# Thozhi 🌼 — Rural Women's Digital Hub

**v2.0 · India-wide · Tamil/Tanglish first · Seven Indian languages + Tanglish**

A small, voice-friendly app and website helping a first-time woman understand government services and learn safe internet use. No login, document uploads, or Aadhaar/OTP/bank-number collection inside Thozhi.

## What is included

- **17 service guides:** Aadhaar, ration/PDS, Ujjwala, health card, doctor access, pensions, rural work, e-Shram, banking/Jan Dhan, women's SHGs, scholarships, skills, DigiLocker, other government services, maternity support, housing and farmer support.
- **All 36 state/UT official directory routes**, plus myScheme/UMANG/National Portal gateways for services beyond the 17 guides.
- **6 original internet lessons:** phone controls; browsing/trusted domains; online forms; documents/downloads/email; passwords/OTP/scams; UPI safety.
- **3 harmless practice activities:** tap/back, a sample-word form, and spotting an OTP scam. No real payment or government form.
- Downloadable service plans and study notes; linked official PDFs, courses and videos from NIELIT, CERT-In, NCW, NPCI, DIKSHA and SWAYAM.
- Tanglish, Tamil, Hindi, Telugu, Kannada, Malayalam, Bengali and Marathi text. All guide/lesson content shares the same safety boundaries. Native-speaker review is still required.
- Responsive website + mobile bottom navigation, installable PWA, and optimized 4K illustrative backgrounds. Not an APK/app-store release.

**Not all government processes are implemented inside Thozhi.** New service pages provide sourced navigation/preparation; actual forms, KYC, payments and approval remain with official departments. Rules, required papers, fees and deadlines vary by state and scheme. No eligibility/payout/job/housing guarantee is made.

The original PMUY guide remains as an in-depth three-question journey. It prepares a connection application; it does not book a refill or submit a government form.

## Run

Node 20.20+:

```bash
npm start
```

Open the shown local/live address. Zero runtime dependencies and **no API key needed**.

```bash
npm test
npm run export:demo
npm run check:submission
```

The export writes `Thozhi-demo.html` beside the project with all fonts, images, models and audio embedded. It is a demo, not an installable HTTPS origin. PWA installation uses the live site in a supported browser; the install-prompt contract is tested with mocks, not actual OS installation.

## Voice, AI and offline

- Twelve bundled Tamil clips cover the original LPG journey plus the new hub and learning introduction. Other detailed readouts use a matching installed phone/browser voice only, never a wrong-language substitute. New languages depend on the device/vendor's voices.
- Speech recognition follows the selected `ta-IN`, `hi-IN`, `te-IN`, `kn-IN`, `ml-IN`, `bn-IN` or `mr-IN` locale and may use a vendor's cloud service. Real microphone/recognition accuracy and regional TTS need phone testing.
- A tiny local TF-IDF/character-feature intent model handles the original guide; a local retrieval router chooses approved hub services/lessons. It does not invent facts or determine new-service eligibility.
- After a successful first load/cache installation, the hub, guides, original lessons, practice, fonts and bundled Tamil audio work offline. Government sites, PDFs, external videos, and cloud speech still need internet.
- State choices, journey answers, lesson-read marks and practice text are session-only. No local/session storage or content logs. Only public assets enter the service-worker cache.
- Typed long numbers and obvious emails are best-effort redacted; this is not comprehensive PII detection. Never type private information in Thozhi. Saved notes are files on the user's phone; shared-phone handling needs training.

Optional Gemini can classify unknown **LPG-guide** questions into approved intents. Copy `.env.example` to `.env`, provide your own key and restart. It requires explicit external-processing consent and a server `allowExternal` flag; it never produces scheme facts. The expanded hub uses local routing and does not send its questions to Gemini. No live Gemini test was performed.

## Sources and quality

See [new services and study-source register](docs/HUB-SOURCES.md), [original PMUY sources](docs/SOURCES.md), and [QA/remaining limitations](docs/QA.md). Source snapshot: **1 October 2026**. Some portals restrict automated retrieval; official account forms and real government submissions are not tested. No WCAG, linguistic, zero-learning or field-study certification is claimed.

The photos are AI-created illustrations, not real beneficiaries or testimonials. Generated originals were resampled to 3840×2160 WebP delivery dimensions; native 4K capture/generation is not claimed. They are not LPG installation instructions.

## Project layout

- `public/app.js`: original guided journey, voice, privacy, installation and handoffs.
- `public/lib/hub*.js`: hub UI, service preparation, local router and rendering.
- `public/lib/learning-data.js`: original lessons and study links.
- `public/lib/states.js`: audited iGOD directory routes.
- `public/lib/scheme*.js`: original deterministic PMUY rules/translations.
- `public/style.css`, `experience.css`, `hub.css`: responsive design.
- `scripts/hub-browser-check.py`: hub, practice, languages, downloads and offline QA.
- Legacy browser checks can use `THOZHI_URL=http://127.0.0.1:3000/?tool=gas`.
- Full QA screenshots are stored outside the repo in `Thozhi-previews/` to keep submission small.

## Submission

Keep **one branch (`main`)**, source/repository below **10 MB**, and create a **public GitHub repository**. At most **two submission attempts**. [Antigravity/GitHub instructions](docs/SUBMISSION.md) explain clone, refine, test, push and signed-out/public verification. No public GitHub publication, Antigravity execution or challenge submission is claimed.

Original code/lessons: MIT. Bundled fonts retain SIL OFL. External textbooks/PDFs are linked, not rehosted.
