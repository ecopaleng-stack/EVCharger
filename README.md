# EV Charger Pro 1.1.0

Android WebView application with:
- Load calculation by charger power or entered current
- Single phase, three-phase 3-wire, and three-phase 4-wire (3P+N) input
- Preliminary voltage-drop calculation and candidate conductor sections based on voltage drop only
- Preliminary materials list
- Editable products catalogue with brand and unit price
- Bill of materials with quantity, unit price, line totals and project total
- Local device storage for catalogue and bill of materials

## Build
GitHub Actions workflow: `.github/workflows/build-apk.yml`.
Run `Build EV Charger Pro APK` from the Actions tab.

## Electrical safety
This app is an estimation aid only. It does not contain validated ampacity tables or a complete protective-device coordination engine. Do not use its preliminary breaker/cable suggestions as installation approval. Verify local code, installation method, grouping, ambient temperature, short-circuit and disconnection requirements, earthing, charger manufacturer requirements, and RCD/DC leakage protection with a qualified electrical engineer.
