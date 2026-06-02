---
name: book-nie-fingerprint-appointment
description: Assist with booking a Spain Extranjería CITA PREVIA appointment for NIE/TIE fingerprinting through the ICP+ website. Use when the user asks to open the Spanish public administration appointment site, choose a province, select a CNP Comisaria office, choose the Policía Nacional fingerprint/TIE card procedure, enter email and applicant identity details, request an appointment, and interactively choose an available date/time.
---

# Book NIE Fingerprint Appointment

## Overview

Guide the user through the Spanish `CITA PREVIA EXTRANJERÍA` ICP+ appointment flow for fingerprinting/TIE card issuance. Treat this as an interactive browser workflow: ask for user choices and personal data only at the step where the site requires them, and never submit a final appointment without explicit confirmation.

## Browser Setup

- Prefer the Codex Browser plugin or another controllable browser surface when available.
- If the user explicitly requires the system Chrome app and the environment cannot control it directly, explain that limitation briefly and use the controllable browser unless the user wants to operate Chrome manually.
- Navigate to:
  `https://sede.administracionespublicas.gob.es/pagina/index/directorio/icpplus`
- Wait for the page to fully load before clicking. If cookie notices, legal notices, or maintenance banners block controls, close or accept only the minimum needed to continue.

## Safety And Consent

- Do not bypass CAPTCHA, anti-bot checks, rate limits, access controls, or website terms.
- Do not invent user data. Ask for `NIE`, `Nombre y apellidos`, `País de nacionalidad`, and email when required.
- Do not store personal data in files unless the user explicitly asks.
- For every final appointment slot, summarize the selected province, office, procedure, date, and time, then ask for explicit confirmation before submitting.
- If no appointments are available, report the site's message and offer to retry manually only if the user asks.
- If the site sends an email confirmation, pause and ask the user to check their mailbox and provide only the code/link/action needed to continue.

## Workflow

### 1. Enter ICP+ Procedure

1. Open the ICP+ directory URL.
2. Click `Acceder al procedimiento`.
3. Wait for the `CITA PREVIA EXTRANJERÍA` page.

### 2. Choose Province

1. Locate the `PROVINCIAS DISPONIBLES` dropdown.
2. Extract the visible province options.
3. Ask the user which province/region to choose. Accept Spanish names, Chinese descriptions, or approximate province names when they clearly map to one option.
4. Select the matching province.
5. Click `Aceptar`.

If the user's choice is ambiguous, show the closest matching options and ask them to choose one.

### 3. Choose Office And Procedure

1. On the office/procedure page, locate `Selecciona Oficina`.
2. Open the dropdown and extract office options whose label includes `CNP`, `Comisaria`, or similar Policía Nacional office wording.
3. Ask the user which office to choose. Include the office names exactly as shown by the site.
4. Select the user's office choice.
5. Locate `TRÁMITES POLICÍA NACIONAL`.
6. Select the option matching:
   `POLICIA-TOMA DE HUELLAS (EXPEDICIÓN DE TARJETA)`

Also accept equivalent capitalization or accent variations, for example `Policia-Toma de huellas (Expedicion de tarjeta)`.

7. Click `Aceptar`.

### 4. Continue Without Cl@ve

1. On the next page, click `Presentación sin Cl@ve` or the closest equivalent button/link.
2. If the site instead requires Cl@ve login or shows a warning, report the exact visible options and pause.

### 5. Email Step

1. When the site asks for an email address, ask the user for the email.
2. Fill the email field exactly as provided.
3. If there is a repeated email field, fill both fields.
4. Click the confirmation/continue button.
5. If the site sends an email, tell the user to check their inbox and wait for the needed confirmation code, link, or instruction.

### 6. Applicant Identity Step

Ask the user for:

- `NIE`
- `Nombre y apellidos`
- `País de nacionalidad`

Then fill the corresponding fields. For nationality, open the dropdown and match the user's country to the site's displayed option. If the country is ambiguous or absent, show likely options and ask.

Click `Aceptar` only after the fields are filled.

### 7. Request Appointment

1. On the next page, choose `Solicitar Cita`.
2. Wait for available appointment dates/times to appear.
3. Extract the available date and time options exactly as shown.
4. Ask the user which date/time they prefer. The user may answer a specific option, or say any date/any time.
5. If the user says any date/any time, choose the earliest available appointment unless the user gives another preference.
6. Before final submission, summarize:
   - Province
   - Office
   - Procedure
   - Applicant name and NIE
   - Email
   - Appointment date/time
7. Ask for explicit confirmation before submitting.

## Interaction Rules

- Keep prompts short and step-specific.
- When extracting dropdown options, present only relevant choices unless the user asks for all choices.
- Use exact site labels in summaries so the user can verify them.
- If a button is disabled, wait briefly, verify required fields, then explain what is missing.
- If page labels differ from this skill, rely on the live page text and preserve the same intent.

## Common Spanish Labels

- `Acceder al procedimiento`
- `CITA PREVIA EXTRANJERÍA`
- `PROVINCIAS DISPONIBLES`
- `Aceptar`
- `Selecciona Oficina`
- `TRÁMITES POLICÍA NACIONAL`
- `POLICIA-TOMA DE HUELLAS (EXPEDICIÓN DE TARJETA)`
- `Presentación sin Cl@ve`
- `Solicitar Cita`
