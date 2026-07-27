HOW TO GET "PROOF" ONTO YOUR PHONE AS A REAL APP
==================================================

This turns your app into a real website with its own address, which you
then add to your phone's home screen. It opens full-screen with its own
icon, just like a normal app — no App Store needed.

You'll do two things: (1) get a free Anthropic API key so the AI
"Describe" feature can work, and (2) put these files online for free
using Netlify.

--------------------------------------------------
STEP 1 — Get an Anthropic API key
--------------------------------------------------
1. Go to https://console.anthropic.com and sign up / log in.
2. Add a small amount of credit (a few dollars covers a LOT of drink
   lookups — each one costs a fraction of a cent).
3. Click "API Keys" in the left sidebar, then "Create Key."
4. Copy the key that starts with "sk-ant-..." somewhere safe. You'll
   paste it into Netlify in Step 3. Don't share this key with anyone
   or post it publicly — it's tied to your billing.

--------------------------------------------------
STEP 2 — Put the app online with Netlify
--------------------------------------------------
1. Go to https://app.netlify.com and sign up for a free account.
2. Once you're on your dashboard, look for a button like
   "Add new site" → "Deploy manually."
3. You'll see a box that says "Drag and drop your site output folder
   here." Unzip the file I gave you (proof-app.zip) so you have a
   regular folder called "proof-app" on your computer, then drag that
   WHOLE FOLDER into the box.
4. Netlify will upload it and give you a live web address, something
   like "https://random-name-123.netlify.app". That's your app's
   address — you can rename it later in Site settings if you want
   something like "proofapp.netlify.app".

--------------------------------------------------
STEP 3 — Add your API key to Netlify (keeps it private)
--------------------------------------------------
1. On your site's page in Netlify, go to "Site configuration" →
   "Environment variables."
2. Click "Add a variable."
3. For the Key, type exactly: ANTHROPIC_API_KEY
4. For the Value, paste the key you copied in Step 1.
5. Save it.
6. Go to the "Deploys" tab and click "Trigger deploy" → "Deploy site"
   so the change takes effect.

--------------------------------------------------
STEP 4 — Add it to your phone's home screen
--------------------------------------------------
On iPhone (Safari):
1. Open your Netlify web address in Safari (must be Safari, not Chrome).
2. Tap the Share icon (square with an arrow) at the bottom.
3. Scroll down and tap "Add to Home Screen."
4. Tap "Add." You'll now have a Proof icon on your home screen that
   opens full-screen, no browser bars.

On Android (Chrome):
1. Open your Netlify web address in Chrome.
2. Tap the three-dot menu in the top right.
3. Tap "Add to Home screen" or "Install app."
4. Confirm. You'll get a home screen icon that opens full-screen.

--------------------------------------------------
THINGS TO KNOW
--------------------------------------------------
- Your drink log, custom drinks, and settings are saved right on your
  phone (in the browser's storage for that app). They won't show up
  on another device, and clearing your phone's browser data would
  clear them too.
- The barcode Scan feature works best in Chrome on Android. Camera
  barcode scanning support in iPhone's Safari is inconsistent — if it
  doesn't work, you can still type the barcode number in by hand.
- If the "Describe" AI feature ever stops working, double-check the
  ANTHROPIC_API_KEY variable is still set in Netlify and that your
  Anthropic account still has credit.
- Anytime you want to change how the app looks or works, just edit
  index.html and re-drag the folder into Netlify to redeploy — or
  come back and ask me to make the changes and re-export the files.
