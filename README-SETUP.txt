FIGHT CAMP 2027 — VERSION 3

WHAT'S NEW
- Supabase email/password account sign-in and cloud sync scaffold.
- Same account can be used on iPhone and laptop.
- Barcode scanning using the phone camera, plus manual barcode entry.
- Open Food Facts product lookup and portion-based macro calculation.
- Existing training, recovery, meals, diary and weight features retained.

IMPORTANT: config.js has already been filled in with your Supabase Project URL and publishable key. The database table and Row Level Security policies were also successfully created in your Supabase project. Do not replace the key with a service_role/secret key.

SETUP SUPABASE (FREE TIER AVAILABLE)
1. Go to https://supabase.com/ and create an account/project.
2. In the project dashboard, open SQL Editor -> New query.
3. Open supabase-schema.sql from this folder, copy all its contents, paste into SQL Editor and click Run.
4. In Supabase Authentication -> URL Configuration, add https://td187255.github.io/fight-camp-2027/ as a Site URL / allowed redirect URL.
5. Upload index.html, config.js, sw.js, manifest.webmanifest and supabase-schema.sql to the ROOT of your GitHub repository and commit.
6. Open the app, go to Targets, create an account, then sign in on both devices with the same account.

DATA SYNC NOTES
- This starter version stores each user's app data as one private JSON record protected by Row Level Security.
- Data is saved locally first and synced to Supabase after a short delay.
- Sign in on a second device to load the same cloud record. If cloud data already exists, it replaces that device's local Fight Camp data. Export a backup first if you have important data on both devices.
- Avoid editing data on both devices at exactly the same time in this first version; later we can add conflict-safe per-record syncing.
- Account email confirmation may be enabled by default in Supabase. If sign-up asks you to confirm email, check your inbox.

BARCODE SCANNER NOTES
- Camera access requires HTTPS (GitHub Pages provides HTTPS) and permission in Safari.
- Open Food Facts is community-maintained; not every barcode is listed and product data can be incomplete. Always check values against the label.
- If camera scanning fails, enter the barcode number manually.

SAFETY / PRIVACY
- Keep your Supabase publishable/anon key only in config.js; never publish a service_role/secret key. The SQL policies restrict each account to its own row.
- This app is a personal tracker, not medical advice. Add only rehab exercises approved by your clinician.
