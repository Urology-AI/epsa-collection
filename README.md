# ePSA Simple Data Collector - Non-PHI

A single-page, offline-first web form for collecting essential ePSA medical data without personal identifiers. Works entirely in the browser—no server required. Exports JSON with only medical metrics.

## Features

- **Offline-first**: No network required after initial load
- **Non-PHI only**: No personal identifiers collected
- **Local storage**: Autosaves draft in browser localStorage
- **Export JSON**: Clean medical data structure
- **BMI auto-calc**: Imperial/metric height/weight with automatic BMI
- **IPSS & SHIM**: Built-in questionnaires (0–5 each)
- **Essential metrics**: Age, race, family history, lifestyle factors

## Usage

1. Open `index.html` in any modern browser
2. Fill in medical information (no personal data required)
3. Click **Save Locally** to persist in browser
4. Click **Export JSON** to download clean medical data
5. Use **Preview JSON** to see the output structure

## Data Structure

```json
{
  "version": "1.0",
  "exportDate": "2025-08-07T12:34:56.789Z",
  "part": "medical-data",
  "collectionInfo": {
    "collectionDate": "2025-08-07",
    "age": 65,
    "race": "black",
    "familyHistory": "no",
    "brcaStatus": "unknown"
  },
  "medicalData": {
    "heightUnit": "imperial",
    "heightFt": "5",
    "heightIn": "9",
    "weight": "180",
    "bmi": 26.6,
    "exercise": "0",
    "smoking": "never",
    "chemicalExposure": "no",
    "ipss": [0,0,0,0,0,0,0],
    "shim": [0,0,0,0,0],
    "psa": "4.5",
    "pirads": "3"
  }
}
```

## Privacy

- **No PHI collected**: No names, IDs, contact information
- **Local storage only**: All data stays in your browser
- **No external requests**: No tracking or server communication
- **Clean exports**: JSON contains only medical metrics

## Sections Collected

1. **Basic Information**: Age, race/ethnicity, collection date
2. **Medical History**: Family history, BRCA status
3. **Physical Measurements**: Height, weight, BMI
4. **Lifestyle Factors**: Exercise, smoking, chemical exposure
5. **Symptoms**: IPSS (urinary), SHIM (sexual health)
6. **Optional Clinical**: PSA, PI-RADS scores

## Deploy

This is a static single-file site. To deploy:

- **GitHub Pages**: Enable Pages from the `main` branch root
- **Netlify/Vercel**: Drag and drop `index.html`
- **Local**: Open `index.html` directly

## License

Internal use. Adapt as needed for research and data collection purposes.
