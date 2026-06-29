# SouthSide Roleplay — GitBook Setup & Branding

This folder is a ready-to-import **GitBook** project. It uses GitBook's standard structure:

```
southside-rules-gitbook/
├── .gitbook.yaml          # GitBook config (points to README + SUMMARY)
├── README.md              # Landing page (with cover image)
├── SUMMARY.md             # The left-hand navigation / table of contents
├── .gitbook/assets/       # Put your logo image here
└── rules/                 # One markdown page per rule section
```

---

## 1. Add your logo

Drop your SouthSide logo image into `.gitbook/assets/` and name it exactly:

```
.gitbook/assets/southside-logo.png
```

(The `README.md` cover and header already reference that filename.) PNG with a transparent or dark background looks best as a cover.

---

## 2. Publish it on GitBook.com

You have two easy options:

### Option A — Git Sync (recommended)
1. Create a free repo on GitHub and push this folder to it (steps below).
2. In GitBook: **New Space → Configure → Git Sync → connect your GitHub repo.**
3. GitBook reads `SUMMARY.md` and builds the whole site automatically.

Push to GitHub:
```bash
cd southside-rules-gitbook
git init
git add .
git commit -m "Initial SouthSide rules"
git branch -M main
git remote add origin https://github.com/<your-username>/southside-rules.git
git push -u origin main
```

### Option B — Import
In GitBook: **Import → from a folder / Markdown**, then upload these files. Git Sync is cleaner because edits stay in version control.

---

## 3. Match the branding to the logo 🌴

GitBook colors are set in the dashboard (**Space → Customize**), not in markdown. Use these values to match the neon-Miami logo:

| Element | Hex | Notes |
| ------- | --- | ----- |
| **Primary / accent** | `#FF1FA2` | Hot neon pink (links, buttons, active nav) |
| **Primary alt** | `#FF4FC3` | Lighter pink for hovers |
| **Secondary accent** | `#A03CFF` | Neon purple |
| **Header background** | `#1A0B2E` | Deep purple-black (matches the night sky) |
| **Page background (dark mode)** | `#150A24` | Very dark purple |
| **Text on dark** | `#F5E9FF` | Soft white-lilac |

Recommended dashboard settings:
- **Customize → Theme:** set **Default mode to Dark** (the neon look pops on dark).
- **Customize → Colors:** primary `#FF1FA2`.
- **Customize → Header:** background `#1A0B2E`, upload the logo as the header logo.
- **Customize → Font:** a clean sans (Inter / Poppins) for body; the logo already carries the script style.
- **Customize → Cover:** the `southside-logo.png` is set as the page cover in `README.md`.

---

## 4. Editing rules later

Each rule lives in its own file under `rules/`. Edit the markdown, commit, push — GitBook updates automatically. To reorder or rename pages, edit `SUMMARY.md`.
