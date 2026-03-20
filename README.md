# DSS — Andaman & Nicobar Ship Boarding System

A single-page boarding management app for the **Directorate of Shipping Services, A&N Islands**.  
Deployed via **GitHub Pages**.

## 📁 Folder Structure

```
dss-boarding/
├── index.html          ← Main app (open this in browser)
├── data/
│   ├── routes.json     ← All voyage routes (editable by admin in-app)
│   └── ports.json      ← All ports: Inter-Island + Mainland sectors
└── README.md
```

## 🚀 GitHub Pages Setup

1. Push this folder to a GitHub repository
2. Go to **Settings → Pages**
3. Set Source to `main` branch, root `/` (or `/docs` if you rename folder)
4. Your app will be live at `https://<username>.github.io/<repo>/`

## 📡 Data Files

- `data/routes.json` — loaded automatically on startup (fetch)
- `data/ports.json` — all port names for dropdowns
- Admin can add custom routes via the **Admin Panel → Routes** tab (stored in localStorage)
- Custom routes override the JSON file

## ✏️ Adding Routes Without Admin Panel

Edit `data/routes.json` directly and push to GitHub.  
Format:
```json
{
  "id": 41,
  "name": "Port A → Port B",
  "stops": ["PORT A", "PORT B"],
  "deboard": "PORT B",
  "valid": ["PORT B"]
}
```

## 🔐 Default Admin Login

Username: `admin`  
Password: (set during first-time setup in the app)
