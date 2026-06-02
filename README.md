# Book NIE Fingerprint Appointment Skill

This repository contains a Codex skill for assisting a user through the Spain `CITA PREVIA EXTRANJERÍA` ICP+ workflow for NIE/TIE fingerprint appointment booking.

## Purpose

The skill is intended to help a user interact with the official Spanish public administration appointment website by:

- Opening the ICP+ appointment page.
- Selecting the province.
- Selecting a CNP/Comisaría office.
- Selecting the `POLICÍA-TOMA DE HUELLAS (EXPEDICIÓN DE TARJETA)` procedure.
- Guiding the user through the `Presentación sin Cl@ve` flow.
- Asking for required applicant information only when needed.
- Reading available appointment slots and helping the user choose one.

## Compliance And Safety Boundaries

This skill is designed for human-in-the-loop assistance. It must not be used as a high-frequency booking bot, appointment scalping tool, or unattended automation system.

The assistant using this skill should:

- Perform only reasonable, user-directed checks.
- Avoid continuous or aggressive refresh loops.
- Never bypass CAPTCHA, anti-bot controls, access restrictions, rate limits, or website terms.
- Never invent or alter applicant identity information.
- Never store personal data unless the user explicitly requests it.
- Stop before final appointment submission and ask the user for explicit confirmation.
- Report official website messages accurately, especially when no appointments are available.

If appointment slots are unavailable, the recommended safe behavior is to stop and inform the user, or to set a low-frequency reminder for manual re-checking. The skill should not repeatedly hammer the government website.

## Personal Data Notice

The workflow may involve sensitive personal information, including:

- NIE
- Full name
- Nationality
- Email address

Only collect this information at the moment the official site requires it. Do not save it to repository files, logs, or public comments.

## Legal Disclaimer

This project is not affiliated with the Government of Spain, the Spanish National Police, or the official ICP+ appointment platform. It does not provide legal advice.

Users are responsible for complying with applicable laws, official website terms, administrative procedure rules, and data protection obligations. For immigration or residency concerns, consult a qualified lawyer or authorized professional.

## Uploading To GitHub

From this project folder:

```bash
git add README.md book-nie-fingerprint-appointment
git commit -m "Add NIE fingerprint appointment skill"
git remote add origin https://github.com/YOUR_USERNAME/book-nie-fingerprint-appointment.git
git push -u origin main
```

Replace `YOUR_USERNAME` and the repository URL with your actual GitHub repository.

If the repository already has a remote named `origin`, update it instead:

```bash
git remote set-url origin https://github.com/YOUR_USERNAME/book-nie-fingerprint-appointment.git
git push -u origin main
```

## Repository Structure

```text
book-nie-fingerprint-appointment/
├── SKILL.md
└── agents/
    └── openai.yaml
```

`SKILL.md` contains the operational workflow and safety rules. `agents/openai.yaml` contains UI metadata for Codex skill discovery.
