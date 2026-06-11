# ChordRoll — Android APK project 🎹📱

This is a **Capacitor Android project** — the exact same setup as your Cloudy AI app
(com.zaza.cloudyai). Build it the same way and you get **app-debug.apk** with the
ChordRoll icon, opening full-screen as a real native app. No browser, works 100% offline
forever (the whole app ships inside the APK).

## Build the APK (same as Cloudy AI)

On your laptop, in this folder:

```
npm install
npx cap sync android
```

Then either:

**Option A — Android Studio:**
```
npx cap open android
```
Build → Build Bundle(s)/APK(s) → Build APK(s)

**Option B — command line:**
```
cd android
gradlew assembleDebug        (Windows)
```

Your APK lands at: `android/app/build/outputs/apk/debug/app-debug.apk`

Copy it to your phone, tap to install, done. App ID: **com.zaza.chordroll**, name: **ChordRoll**.

## Editing the app

The whole app is `www/index.html`. To add progressions, edit the `PROGS` array:

```js
{name:'My Progression', genre:'Afrobeats', moods:['Groovy','Dark'],
 steps:[[0,'m','i'],[8,'','VI'],[3,'','III'],[10,'','VII']]}
```

After any edit, run `npx cap sync android` and rebuild the APK.

## What's inside

- 106 progressions, 24 genres (Afrobeats, Amapiano, Dancehall, Reggae, Hip Hop, Trap,
  Drill, R&B/Soul, Neo-Soul, Gospel, Pop, Rock, EDM/House, Jazz, Lo-fi, Blues, Country,
  Latin/Reggaeton, Cinematic, Highlife, Funk, Afro House, Smooth Rock, Classics 1958)
- Mood filters: Happy, Sad, Chill, Dark, Euphoric, Romantic, Hype, Groovy, Nostalgic, Epic, Uplifting, Dreamy
- FL Studio-style piano roll, all 12 keys, built-in playback with BPM + loop
- Custom ChordRoll launcher icons already installed at every density

## GitHub

Push this whole folder to a repo (node_modules is already excluded by .gitignore).
The same `www/` folder also works on GitHub Pages if you ever want a web version too.
