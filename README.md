# Dose Curve

A small offline web app (PWA) that plots an estimated Adderall IR blood-level curve over 24 hours.
Everything runs on the phone. Nothing is stored or sent anywhere.

## Put it on GitHub Pages (from your iPhone)

1. Unzip `dose-curve.zip` in the Files app.
2. On github.com, tap **+** → **New repository**.
   - Name: `dose-curve`
   - Visibility: **Public** (free Pages needs this; it's only the app code)
   - Tap **Create repository**.
3. Tap **uploading an existing file**.
4. Pick all 8 files from the unzipped folder. Tap **Commit changes**.
5. Go to **Settings** → **Pages**.
   - Source: **Deploy from a branch**
   - Branch: **main**, folder **/ (root)** → **Save**
6. Wait about a minute. Open `https://YOUR-USERNAME.github.io/dose-curve/` in **Safari**.
7. Tap **Share** → **Add to Home Screen** → **Add**.

Open it once from the home screen while online. After that it works in airplane mode.

## Updating it later

1. Upload the changed files to the repo.
2. In `sw.js`, change `dose-curve-v1` to `dose-curve-v2` (and so on).
3. Open the app twice. The second launch shows the new version.

## Run it on a computer

```
cd dose-curve
python3 -m http.server 8000
```

Then open http://localhost:8000.

## The model

- One-compartment curve with first-order absorption, added up across doses.
- Peak about 3 h after a dose. Half-life 10.4 h (d-amphetamine) and 12.65 h (l-amphetamine), mixed 3:1.
- These are average adult numbers from the FDA label for Adderall tablets.
- The y-axis is "% of one 10 mg peak". It's a planning aid, not dosing advice.
