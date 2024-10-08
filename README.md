# Git Stash Übung

Willkommen zu dieser Übung zum Thema **Git Stash**! In dieser Aufgabe wirst du lernen, wie du unvollständige Änderungen mit `git stash` speichern und später wieder anwenden kannst. Außerdem wirst du Änderungen in verschiedenen Branches durchführen.

## Ziel der Übung

- **Ziel 1:** Verstehen, wie `git stash` funktioniert, um unvollständige Arbeit temporär zu speichern.
- **Ziel 2:** Üben, wie du in einem neuen Feature-Branch arbeiten kannst, Änderungen stashst und zu einem anderen Branch wechselst, um dort dringende Arbeiten zu erledigen.

## Aufgabenbeschreibung

### Schritt 1: Klone das Repository

1. **Forke** dieses Repository in deinen eigenen GitHub-Account.
2. **Klone** das geforkte Repository auf deinen lokalen Rechner:

   ```bash
   git clone https://github.com/<DeinGitHubName>/git-stash-uebung.git
   cd git-stash-uebung
   ```

### Schritt 2: Erstelle einen Feature-Branch

```bash
git checkout -b feature-aenderung
```

### Schritt 3: Nimm Änderungen an index.html vor

Füge einen neuen Paragraphen in die Datei index.html hinzu:

```html
<p>Änderung für das neue Feature</p>
```

### Schritt 4: Stashe deine Änderungen

Bevor du die Änderungen committest, wirst du gebeten, eine dringende Änderung im main-Branch vorzunehmen. Um deine Änderungen zu speichern, ohne sie zu committen, nutze git stash:

```bash
git stash
```

### Schritt 5: Wechsle zum main-Branch und nimm eine Bugfix-Änderung vor

Wechsle zurück zum main-Branch, um die Bugfixes durchzuführen:

```bash
git checkout main
```

Öffne die Datei style.css und füge eine neue Regel für die Hintergrundfarbe hinzu:

```css
body {
    background-color: #f0f0f0;
}
```

### Schritt 6: Kehre zu deinem Feature-Branch zurück und wende den Stash an

Nachdem du die Änderungen im main-Branch erledigt hast, kehre zu deinem Feature-Branch zurück und stelle deine gestashten Änderungen wieder her:

```bash
git checkout feature-aenderung
git stash apply
```

### Schritt 7: Committe und pushe deine Änderungen

Nachdem du die gestashten Änderungen angewendet hast, committe deine Arbeit und pushe sie zu deinem Repository:

```bash
git add index.html
git commit -m "Füge neue Feature-Änderung hinzu und wende Stash an"
git push origin feature-aenderung
```

### Abgabe
mache Screenshots von deinen Befehlen, mache regelmäßig log Ausgaben
und gebe sie gemeinsam mit dem Link zu deinem Repo in Teams ab







