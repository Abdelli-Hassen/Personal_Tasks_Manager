# Suivi des tâches

Daily task tracker (day / week / board views, urgent tasks, export to Excel/CSV) that reads and saves
**directly into a CSV file on your own computer**. Your data never leaves your machine and is never uploaded.

**Use it here: https://personaltasksmanager.vercel.app**

## First use

1. Open the link above in **Chrome or Edge** (desktop).
2. Click **Choisir mon fichier CSV** and pick your file, or **Je n'ai pas de fichier : en créer un** to start fresh.
   Accept the browser's "edit this file" prompt. If Chrome offers **Allow on every visit**, choose it.
3. Every change is written to that file about a quarter of a second later.

Next visits: the app remembers the file. If the browser asks again, you get one screen
*"Est-ce le bon fichier ?"* with the file name and one button to confirm.

Tip: use the install icon in the address bar to install it as an app.

## Good to know

- Close the CSV in Excel while using the app (Excel locks the file). If you edit the file elsewhere,
  the page refreshes itself within a couple of seconds.
- Firefox and Safari can't write to local files; there you can only use **Exporter**.
- The status box at the top lets you **Changer** the linked file or **Délier** it to start from zero.
- CSV columns: `Week-date;PDV;Tache;Situation;commentaire;Date;Heure;Urgent`.
