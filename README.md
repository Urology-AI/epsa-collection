# ePSA Offline Part 1 Collector

A single-page, offline-first web form for collecting ePSA Part 1 data. Works entirely in the browser—no server required. Saves locally and exports JSON in the same structure as your ePSA Part 1 export.

## Features

- **Offline-first**: No network required after initial load
- **Local storage**: Autosaves draft in browser localStorage
- **Export JSON**: Matches ePSA Part 1 export schema
- **BMI auto-calc**: Imperial/metric height/weight with automatic BMI
- **IPSS & SHIM**: Built-in questionnaires (0–5 each)
- **Consent gating**: Export requires consent checkbox

## Usage

1. Open `index.html` in any modern browser
2. Fill in patient info and form fields
3. Click **Save Locally** to persist in browser
4. Click **Export JSON** to download a file
5. Use **Preview JSON** to see the output structure

## Data Structure

```json
{
  "version": "1.0",
  "exportDate": "2025-08-07T12:34:56.789Z",
  "part": "part1",
  "patientMeta": {
    "name": "...",
    "phone": "...",
    "mrn": "...",
    "dateOfService": "...",
    "consent": true
  },
  "formData": {
    "age": "...",
    "race": "...",
    "familyHistory": 0,
    "inflammationHistory": 0,
    "heightUnit": "...",
    "heightFt": "...",
    "heightIn": "...",
    "heightCm": "...",
    "weightUnit": "...",
    "weight": "...",
    "weightKg": "...",
    "bmi": "...",
    "exercise": 0,
    "ipss": [0,0,0,0,0,0,0],
    "shim": [0,0,0,0,0],
    "psa": "...",
    "pirads": "..."
  }
}
```

## Privacy

- All data stays in your browser unless you export it
- No external requests or tracking
- Optional: Ask me to hash phone/MRN before export if you want to reduce PHI in JSON files

## Deploy

This is a static single-file site. To deploy:

- **GitHub Pages**: Enable Pages from the `main` branch root
- **Netlify/Vercel**: Drag and drop `index.html`
- **Local**: Open `index.html` directly

## License

Internal use. Adapt as needed for your institution.
