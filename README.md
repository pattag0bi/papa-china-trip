# Papa's China Trip

A one-page, phone-friendly guide for Papa's China trip (24 Oct to 3 Nov 2026).
Everything is in `index.html`: no build step, no internet libraries, nothing to install.

## Before you send it: 2 things to fill in

Open `index.html` in any text editor and search for `TRIP`.

1. **Your WhatsApp number.** Find `helperWhatsApp: "TBD"` and put your number in:
   digits only, with country code, no `+`, no spaces. Example format: `"919812345678"`.
   Until you do this, the WhatsApp buttons still work, but Papa has to pick your contact himself.
2. **Anything marked `{TBD}`.** Search for `TBD`. Each one shows a grey "To be confirmed"
   chip on the page. Replace it with the real fact, or leave it if still unknown.
   Current TBDs: flights, Shanghai hotel, which companies to visit (Option B),
   Shenzhen to Guangzhou transport (Option C), drone/robot import rules, eSIM and Airtel prices.

## How to edit the TRIP object

All words on the page live in one JavaScript object called `TRIP`, at the top of the
`<script>` block. It is split into sections that match the 7 steps:

| Section in TRIP | Step on the page |
|---|---|
| `glance` | 1. Your trip at a glance |
| `conference` | 2. The conference |
| `freeDays` | 3. Choose your free days |
| `internet` | 4. Internet in China |
| `apps` | 5. Chinese apps on your iPhone |
| `know` | 6. Things to know before you go |
| `send` | 7. Send your choices to Raunak |

Rules:

- Change only the text inside the quotes. Keep the commas and brackets as they are.
- `{TBD}` inside text shows the grey "To be confirmed" chip.
- `**words**` shows those words in **bold**.
- Most cards have `lines` (always shown) and `more` (hidden under "Tell me more"). `moreList` adds a bullet list under "Tell me more".
- Add `tone: "red"` to a card for "Must do", or `tone: "amber"` for "Important".
- Option meters (`effort`, `cost`, `business`) go from 0 to 3.
- To add a checklist item, add a line to `send.checklist`. It shows up in the WhatsApp message too.
- Keep copy plain: short sentences, no em dashes, and no jargon without an explanation.

If you change the structure a lot and Papa's old answers look wrong, change
`storageKey` (for example to `"papa-china-trip-v2"`) to start fresh.

After editing, open `index.html` in your browser to check it. Use your browser's
phone view (about 390 px wide) to see what Papa will see.

## How to send the page to Papa

Papa needs a link, not a file. Two easy free ways:

### Option 1: Netlify Drop (fastest, about 1 minute)

1. Go to <https://app.netlify.com/drop>.
2. Drag the folder that holds `index.html` onto the page.
3. Netlify gives you a link like `https://something-random.netlify.app`.
4. Send that link to Papa on WhatsApp.

Without an account, a Drop site may be deleted after a while. Sign up (free) to keep it.
To update the page later, sign in, open the site, go to **Deploys**, and drag the folder again.
The link stays the same.

### Option 2: GitHub Pages

1. Create a new public repository on GitHub, for example `papa-china-trip`.
2. Upload `index.html` (Add file › Upload files › Commit).
3. Go to **Settings › Pages**. Under "Branch", pick `main` and `/ (root)`, then Save.
4. After a minute your link is `https://<your-username>.github.io/papa-china-trip/`.
5. Send that link to Papa on WhatsApp.

To update, upload the new `index.html` again. The link stays the same.

Note: a public link can be opened by anyone who has it. The page includes the
organiser's contact details, so share the link only with Papa.

### Tip for Papa

Ask him to open the link in Safari, tap the Share button, then **Add to Home Screen**.
It then opens like an app. His answers are saved on his phone, so he can stop and come back.
