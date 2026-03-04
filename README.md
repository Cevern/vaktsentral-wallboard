# 🏢 Vaktsentral Wallboard – Mustad Eiendom

Operativt dashboard-system for Vaktsentral.

## Sider

| Side | Fil | Beskrivelse |
|------|-----|-------------|
| Command Center | `index.html` | Driftmeldinger + hendelseslogg fra SharePoint via Power Automate |
| Asana Oppgaver | `index2.html` | Live oppgaveoversikt fra Asana |

## 🚀 GitHub Pages

Siden kjører på: `https://cevern.github.io/vaktsentral-wallboard/`

## ⚙️ Oppsett

### Command Center (`index.html`)
Åpne siden og lim inn Power Automate Flow URL. Eller bruk URL-parameter direkte:
```
index.html?url=https://din-flow-url
```

### Asana Dashboard (`index2.html`)
1. Gå til [app.asana.com/0/my-apps](https://app.asana.com/0/my-apps) → **+ Create new token**
2. Finn prosjekt-ID i Asana URL: `asana.com/0/PROSJEKT_ID/...`
3. Åpne siden og fyll inn token + prosjekt-ID(er)

Eller koble opp skjermer direkte med URL-parametere:
```
index2.html?token=DITT_TOKEN&projects=ID1,ID2&interval=60
```

## 🖥️ Koble til skjermer

Åpne ønsket URL i nettleser på skjermen og trykk **F11** for fullskjerm.  
Siden oppdaterer seg automatisk og laster på nytt kl **04:00** hver natt.

## 📁 Filstruktur

```
vaktsentral-wallboard/
├── index.html          ← Command Center (SharePoint / Power Automate)
├── index2.html         ← Asana Oppgavedashboard
├── README.md           ← Denne filen
└── .github/
    └── workflows/
        └── deploy.yml  ← Auto-deploy til GitHub Pages
```