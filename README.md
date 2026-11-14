# Sandbox Processing — v1

A deliberately small iPad-friendly garment processing app.

## Fields
- Type: Sweater / Scarf / Other
- Item ID
- Quick photo from camera/photo library
- Sweater: P2P, length, shoulders, sleeve length
- Scarf: length, width
- Other: free-form notes / measurements
- Known defects
- Strengths

## What it does
- Saves records locally in the browser using IndexedDB
- Compresses the quick photo before storing it
- Prevents accidentally creating a second record with the same ID
- Lets you reopen and edit recent items
- Exports structured records to CSV for Google Sheets

## Important
The current v1 is intentionally local-first. It does NOT yet sync directly to Google Sheets.
For the simplest next step, export CSV and import/append it to a Google Sheet.
A later v2 can add direct Google Sheets sync or be recreated in AppSheet using the same columns.

## iPad use
For the camera button and “Add to Home Screen” experience, serve these files from any HTTPS web host
(GitHub Pages, Cloudflare Pages, Netlify, etc.). Open the URL in Safari and choose:
Share → Add to Home Screen.

The form itself is fully client-side; no server receives your garment data.

v1.3
- Recent items still shows the newest 20 by default.
- Added Item ID search across all stored records.
- Added Show all / Show recent toggle.
- CSV export and IndexedDB data are unchanged.
