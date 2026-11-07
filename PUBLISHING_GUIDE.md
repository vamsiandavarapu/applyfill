# How to publish ApplyFill on Microsoft Edge Add-ons (free)

Total cost: **0**. Microsoft charges no registration fee for the Edge program. Review can take up to 7 business days.

## What is in this kit
| File / folder | Use |
|---|---|
| `applyfill-extension-v1.0.0.zip` (sent separately) | The package you upload to Partner Center |
| `index.html` | Root landing page for the GitHub Pages site |
| `privacy-policy.html` | Host it publicly; paste its URL into the Privacy tab |
| `STORE_LISTING.md` | Every piece of text the listing asks for |
| `store-assets/` | Logo (300x300) and 5 screenshots (1280x800) |
| `demo-site/` | A harmless fake job site for reviewers to test on |
| `demo-profile.json` | A fictional profile reviewers can import |

## Step 1: Test it yourself first (15 minutes)
1. Open `edge://extensions`, turn on Developer mode, **Load unpacked**, pick the unzipped extension folder.
2. The Settings page opens. **Import from file** your own `my-profile.json`, press **Save profile**.
3. Try it on the demo site and on 2 or 3 real company career pages (Greenhouse or Lever postings are easiest).
4. Optional: turn on AI, choose Groq, model `openai/gpt-oss-120b`, paste your key, press **Test connection**.
Fix anything odd before you submit. Every rejected submission costs days.

## Step 2: Host the privacy policy and demo site (free, 10 minutes)
1. Create a GitHub account if needed, then a new **public** repository named `applyfill`.
2. Upload `index.html`, `privacy-policy.html` and the `demo-site` folder.
3. Repository **Settings > Pages > Deploy from a branch > main / root > Save**.
4. After a minute your pages are live at:
   - `https://YOUR-USERNAME.github.io/applyfill/` (site landing page)
   - `https://YOUR-USERNAME.github.io/applyfill/privacy-policy.html` (privacy policy URL)
   - `https://YOUR-USERNAME.github.io/applyfill/demo-site/index.html` (demo site for reviewers)
Open all three links in a private window to confirm they load, and confirm the privacy policy shows the real contact name and email.

## Step 3: Check the name
Search the Edge Add-ons store for **ApplyFill**. If it is taken or too similar, pick another name and change `"name"` in `manifest.json` (and `STORE_LISTING.md`), then re-zip. Do not use names or logos of other companies or browsers.

## Step 4: Create your developer account (free)
1. Sign in at **Partner Center > Microsoft Edge program** with a personal Microsoft account (Outlook, Live or Hotmail). Work or school accounts cannot register.
2. Choose account type **Individual**. This cannot be changed later.
3. Fill in country, publisher display name (up to 50 characters, this is shown to users), contact details, and accept the developer agreement.
4. Wait for the confirmation email. Individual verification is usually short.

## Step 5: Submit the extension
1. Partner Center: **Create new extension**, upload `applyfill-extension-v1.0.0.zip`. Fix any validation message.
2. **Availability**: Public, all markets.
3. **Properties**: category Productivity, website and support contact from `STORE_LISTING.md`.
4. **Privacy tab**: paste the single purpose and permission justifications from `STORE_LISTING.md`, say no remote code, tick the data types listed there, certify the three statements, and paste your privacy policy URL.
5. **Store listings (English)**: paste the description and search terms, upload the logo and the 5 screenshots in order.
6. **Notes for certification**: paste the text from `STORE_LISTING.md`, with your demo site URL filled in.
7. Mark the language **Complete** and press **Publish**.

## Step 6: After you submit
- Status moves through review to **In the Store** (up to 7 business days). If you get a rejection, the email names the policy section. Fix it, bump the version, and resubmit.
- Share your store link. Users install with **Get**; the Settings page opens on first run.

## Updating later
1. Change the code, raise `"version"` in `manifest.json` (for example 1.0.1).
2. Re-zip so `manifest.json` is at the top level, upload the new zip in Partner Center, add a note describing the change, and submit again.
3. If you ever add a new permission or send new data anywhere, update the privacy policy, the Privacy tab and the in-extension wording first.

## Rules you must keep following
- Never send user data anywhere except as described in the privacy policy.
- Never add remote code or obfuscated code.
- Keep every permission justified by a real feature.
- Do not claim the tool works on sites you have not tested.

## Support tips
- Most user problems will be: forgot to save the profile, AI key typed wrongly, or a site with fancy custom dropdowns (these show orange; the user fills them).
- Ask users to include the site name and the orange field labels when they report a problem, so you can add matching rules.
