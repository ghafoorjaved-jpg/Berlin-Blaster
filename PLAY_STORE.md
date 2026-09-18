# Upload Berlin Word Blaster to Google Play

Google Play does not accept a raw HTML file. You wrap the published website as an Android app (Trusted Web Activity).

## 1. Put the game on HTTPS

Push this repo to GitHub and turn on **GitHub Pages**.  
You need a public URL such as:

`https://YOUR_USER.github.io/berlin-word-blaster/`

Open that URL on a phone and confirm the game runs.

Host `docs/PRIVACY.md` as a page too, or paste it into a simple `privacy.html`. Play Console requires a privacy-policy URL.

## 2. Install Bubblewrap

On your computer (Node.js 18+):

```bash
npm i -g @bubblewrap/cli
bubblewrap init --manifest https://YOUR_USER.github.io/berlin-word-blaster/manifest.json
```

Use:

- Application name: `Berlin Word Blaster`
- Package ID: `com.yourname.wordblaster` (must be unique, all lowercase)
- Display: standalone
- Orientation: portrait

## 3. Build the Android App Bundle

```bash
bubblewrap build
```

This produces an `.aab` file. That is what Play Console wants.

Keep the keystore file Bubblewrap creates. If you lose it you cannot update the app.

## 4. Play Console listing

Create an app at [https://play.google.com/console](https://play.google.com/console).

Fill in:

- Title: Berlin Word Blaster
- Short description: Shoot the German word. Learn A1 to C2.
- Full description: Pang-style balloon game that teaches German nouns with articles. 600 stages from A1 to C2. Spoken German on a correct hit.
- Category: Education / Game
- Privacy policy URL
- Phone screenshots (open the live site, screenshot portrait)
- Feature graphic 1024×500
- Content rating questionnaire

Upload the `.aab` under **Production** or **Testing**.

## 5. What this zip does not include

- A finished signed `.aab` (needs your signing key on your machine)
- A Play Developer account ($25 one-time, Google)
- Store screenshots from your phone

## Alternative: Capacitor

```bash
npm init @capacitor/app
# copy index.html and icons into the web folder
npx cap add android
npx cap sync
```

Then open the Android project in Android Studio and generate a signed bundle.
