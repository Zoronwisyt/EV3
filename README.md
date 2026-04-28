# Edit Vault — Setup Guide

A modern, shareable editing resource hub. Works 100% on GitHub Pages — no server needed.

---

## ⚡ Quick Setup (5 minutes)

### 1. Get a free JSONBin API key

1. Go to **[jsonbin.io](https://jsonbin.io)** and sign up for a free account
2. Go to **API Keys** in your dashboard
3. Copy your **Master Key** (starts with `$2a$10$...`)

### 2. Add your key to `index.html`

Open `index.html` and find this line near the top of the `<script>` tag:

```js
const MASTER_KEY = '$2a$10$REPLACE_WITH_YOUR_JSONBIN_MASTER_KEY';
```

Replace the placeholder with your actual key:

```js
const MASTER_KEY = '$2a$10$abc123yourrealkeyhere...';
```

### 3. (Optional) Add a Collection ID

In JSONBin, create a Collection to keep all vaults organized. Paste the Collection ID here:

```js
const COLLECTION_ID = 'your_collection_id_here';
```

### 4. Deploy to GitHub Pages

1. Create a new GitHub repo (e.g. `edit-vault`)
2. Upload `index.html` as the only file
3. Go to **Settings → Pages → Source → main branch / (root)**
4. Your site is live at `https://yourusername.github.io/edit-vault`

---

## 🔑 How Vaults Work

| Feature | Detail |
|---|---|
| **Create vault** | Generates a new JSONBin "bin" and stores the vault ID in your browser |
| **Unique link** | `https://yoursite.com?v=VAULT_ID` |
| **Share** | Anyone with the link can view the vault and add resources |
| **Owner** | The browser that created the vault is the owner (can edit/delete) |
| **Files** | Stored as base64 inside JSONBin — keep under 8MB per file |
| **Links** | External URLs that open in a new tab |

---

## 📦 JSONBin Free Plan Limits

- **10,000 requests/month** — plenty for personal use
- **100KB per bin** — fits ~50–100 resources comfortably
- **Unlimited bins** — each vault is its own bin

---

## 🛠️ Customization

To change the site name, find this in `index.html`:
```html
<title>Edit Vault</title>
```

To change the logo text:
```html
<h1>Edit Vault</h1>
```
