# VPR Fresh Farm — Website

## 1. Add your real product photos
Put your own photos in the `images/` folder using **exactly** these filenames (jpg):

- `images/onion.jpg`
- `images/brinjal.jpg`
- `images/groundnut.jpg`
- `images/maize.jpg`
- `images/tomato.jpg`
- `images/turmeric.jpg`

If a photo is missing, the site automatically shows a drawn illustration instead — so nothing breaks, you can add photos whenever you have them.

## 2. Set your real UPI ID
Open `index.html`, find this near the top of the `<script>` section:

```js
const UPI_ID = "vprfreshfarm@upi"; // DUMMY — replace with your real UPI ID
```

Replace `vprfreshfarm@upi` with your real UPI ID (e.g. `yourname@oksbi`, `yourname@paytm`, etc). The QR code and "Pay via UPI App" button update automatically from this value.

Your WhatsApp number is already set to **9944461720**.

## 3. Important: how order storage works
This is a static website (no server/database). Orders are saved using the browser's **local storage**, meaning:

- Orders only save on the same device/browser that placed them.
- The `admin.html` dashboard only shows orders placed from that same browser.
- It will **not** automatically collect orders from every customer's phone into one place.

This is fine for testing, tracking orders you take yourself, or a single shared shop device. If you want every customer's order to land in one central dashboard automatically, you'd need a real backend (e.g. Google Sheets + Apps Script, or Firebase) — ask me and I can set that up separately.

## 4. Uploading to GitHub (step by step)

1. **Create a GitHub account** at https://github.com if you don't have one.
2. **Create a new repository**:
   - Click the **+** icon (top right) → **New repository**.
   - Name it e.g. `vprfreshfarm`.
   - Set it to **Public**.
   - Don't add a README (you already have one) — click **Create repository**.
3. **Upload your files**:
   - On the new repo page, click **uploading an existing file**.
   - Drag in `index.html`, `admin.html`, `README.md`, and the whole `images` folder.
   - Scroll down, click **Commit changes**.
4. **Turn on GitHub Pages** (to get a live web link):
   - In your repo, go to **Settings** → **Pages** (left sidebar).
   - Under "Build and deployment", set **Source** to **Deploy from a branch**.
   - Set **Branch** to `main` and folder to `/ (root)`, click **Save**.
   - Wait 1–2 minutes, then refresh — GitHub will show your live URL, usually:
     `https://YOUR-USERNAME.github.io/vprfreshfarm/`
5. **Share that link** — it works for any visitor, on any device, anywhere.

### Making changes later
Any time you want to update prices, photos, or text: open the file on GitHub (click it → pencil/edit icon), make your change, and commit — the live site updates automatically within a minute or two.
