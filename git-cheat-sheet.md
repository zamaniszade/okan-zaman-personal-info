# Mein Git-Cheat-Sheet

## git clone
git clone kopiert ein Repository von GitHub auf meinen Rechner. Dabei entsteht ein neuer Ordner mit allen Dateien und der Verbindung zu GitHub (versteckter Ordner .git).
Beispiel:
git clone https://github.com/zamaniszade/okan-zaman-personal-info.git
Danach: cd okan-zaman-personal-info

## git status
git status zeigt, in welchem Zustand meine Dateien gerade sind. Es verändert nichts.
Beispiel:
git status
Ausgabe aus meiner Übung:
Untracked files:
        index.html
- Untracked: Git kennt die Datei noch nicht.
- Changes to be committed: Die Datei ist staged (vorgemerkt).
- ahead of 'origin/main' by 1 commit: Ich habe einen Commit, der noch nicht auf GitHub ist.
- up to date with 'origin/main': Lokal und GitHub haben denselben Stand.

## git add
git add legt eine Datei in die Staging Area (vorgemerkt für den nächsten Commit). Gespeichert ist sie damit noch nicht.
Beispiel:
git add index.html images/
Danach steht die Datei bei git status unter "Changes to be committed".
Wichtig: Ohne Dateiname passiert nichts. "git add ." würde alles hinzufügen.

## git commit
git commit speichert alles aus der Staging Area als Commit im lokalen Repository. Der Commit ist nur auf meinem Rechner, nicht auf GitHub.
Beispiel:
git commit -m "Add personal information page"
- -m steht für message (Nachricht).
- Die Nachricht sollte beschreiben, was sich geändert hat.

## git log
git log zeigt den Verlauf meines Repositorys: eine Liste aller Commits, der neueste steht oben. Es ist wie das Tagebuch meines Projekts.
zB.:
commit aec16b4a...
Author: zamaniszade <zamaniszade@gmail.com>
Date:   Thu Nov 19 01:16:44 2026 +0100

    Add personal information page
- commit + Hash: die eindeutige Kennung dieses Commits.
- Author: wer ihn gemacht hat.
- Date: wann.
- Eingerückter Text: die Commit-Nachricht. Deshalb sollte sie beschreiben, was sich geändert hat.

## git push
git push schickt meine lokalen Commits zu GitHub. Erst danach sind sie dort sichtbar.
Beispiel:
git push
Ausgabe aus meiner Übung:
   7c23f73..aec16b4  main -> main
Das heißt: Mein neuer Commit aec16b4 liegt jetzt auf GitHub.
Danach sagt git status: "Your branch is up to date with 'origin/main'".

## git pull
git pull holt neue Commits von GitHub auf meinen Rechner und fügt sie in meinen lokalen Stand ein. Nützlich, wenn jemand anderes oder ich selbst woanders etwas hochgeladen habe.
Beispiel:
git pull
Wenn nichts Neues da ist: "Already up to date."

## Ablauf: neue Datei auf GitHub bringen
git add index.html
git commit -m "Add personal information page"
git push