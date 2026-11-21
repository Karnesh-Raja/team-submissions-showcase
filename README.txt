TEAM SUBMISSIONS PORTAL — QUICK SETUP

This is a single-file GitHub Pages website. It reads a publicly published CSV tab from Google Sheets and checks for updates every 30 seconds. Google's published copy may itself take a few minutes to update.

1. In your linked response spreadsheet, add a new sheet/tab named Public Data.
2. In Public Data!A1, enter:
   =QUERY('Form Responses 1'!C:E,"select Col1, Col2, Col3 where Col1 is not null",1)
   If your response tab has a different name, replace Form Responses 1 with the exact tab name. Keep the single quotes around the name.
3. Confirm Public Data has only these three columns: Team Name, PPT link, Video link. Do not add Email Address.
4. In Google Sheets, choose File > Share > Publish to web.
5. Choose the Public Data tab (not Entire document), choose Comma-separated values (.csv), and click Publish.
6. Copy the published CSV URL.
7. Open index.html and replace PASTE_YOUR_PUBLISHED_CSV_URL_HERE in the SHEET_CSV_URL setting with the copied URL. Keep the quotes around the URL.
8. Create a public GitHub repository, upload index.html, and enable GitHub Pages from Settings > Pages > Deploy from a branch > main > /(root) > Save.
9. Open the Pages URL after GitHub finishes publishing.

NOTES
- The page displays only team names and the two links. It does not read or display email addresses.
- If the submitted PPT or video is stored in Google Drive, set its General access to Anyone with the link / Viewer only when it is appropriate for public viewing. Do not publish sensitive personal information.
- Keep Automatically republish when changes are made enabled in the Google Sheets Publish to web settings.
- To stop public data publishing later, return to File > Share > Publish to web > Published content & settings > Stop publishing.
