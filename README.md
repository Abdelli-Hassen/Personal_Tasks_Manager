# Suivi des tâches

Daily task tracker (day / week / board views, export to Excel/CSV) that reads and saves
**directly into a CSV file on your own computer**. The site is static; your data never
leaves your machine and is never uploaded.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | the whole app |
| `manifest.webmanifest`, `icon.svg`, `sw.js` | make it installable as an app and usable offline |
| `vercel.json` | static hosting config and headers |
| `.gitignore` | keeps `*.csv` / `*.xlsx` out of git |

No build step, no dependencies.

## Deploy

```powershell
cd suivi-taches-site
git init
git add .
git commit -m "Suivi des tâches"
git branch -M main
git remote add origin https://github.com/<you>/<repo>.git
git push -u origin main
```

Then on vercel.com: **Add New → Project → import the repo**. Framework preset: *Other*,
leave build command and output directory empty, click **Deploy**.
The repo can be private.

## First use

1. Open the Vercel URL in **Chrome or Edge** (desktop).
2. Click **Choisir mon fichier CSV**, pick `Taches accompli(Sheet1).csv`, and accept the browser's
   "edit this file" prompt. In that prompt choose **Allow on every visit** if Chrome offers it.
3. Every change is written to that file about a quarter of a second later.

Next visits: the app remembers the file. If the browser asks again, you get one screen
*"Est-ce le bon fichier ?"* with the file name and one button to confirm.

## Good to know

- Browsers never allow a website to write to a local file without the user's consent. That one
  confirmation is the minimum; it cannot be removed. Installing the site as an app
  (address bar → install icon) and choosing "Allow on every visit" makes it rare.
- Close the CSV in Excel while using the app (Excel locks the file). Reopen it afterwards to see changes.
- Firefox and Safari can't write to local files; there you can only use **Exporter**.
- CSV columns: `Week-date;PDV;Tache;Situation;commentaire;Date;Heure`.
