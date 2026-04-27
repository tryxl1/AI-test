# UFO Voice Avatar AI (Windows 11)

Desktop aplikace pro Windows 11 (Electron), která:

- umožní uložit **API Key** (OpenAI‑compatible)
- přijímá řeč z **mikrofonu** (push‑to‑talk) a přepíše ji na text (Web Speech API, fallback na psaní)
- pošle text do **AI chatu**
- odpověď **přečte nahlas** (SpeechSynthesis)
- zobrazí jednoduchý **avatar**, který “mluví” (animace při TTS)

## Požadavky

- Windows 11
- Node.js LTS (doporučeno 20+), aby fungovalo `npm`

Ověření:

```bash
node -v
npm -v
```

## Spuštění (dev)

```bash
npm install
npm run dev
```

## Build instalačky

```bash
npm run build
```

Výstup najdete v `dist/`:

- `UFO Voice Avatar AI Setup ... .exe` (instalátor – NSIS)
- `UFO Voice Avatar AI ... .exe` (**portable single EXE**, spustíte přímo bez instalace)

Pokud chcete jen single EXE:

```bash
npm run build:exe
```

## Použití bez instalace (doporučeno)

Koncový uživatel **nic neinstaluje** – stačí stáhnout **portable `.exe`** a spustit ho.

Nejjednodušší cesta je mít repozitář na GitHubu a použít přiložený workflow `Build Windows EXE`, který po tagu `v*`
vyrobí `.exe` jako artifact ke stažení.

## Bezpečnost poznámka

API key je uložený lokálně v uživatelském profilu přes Electron `safeStorage` (když je dostupné).

