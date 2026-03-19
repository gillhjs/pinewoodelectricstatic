# Pinewood Electrical — Deployment Guide
## GitHub → GoDaddy (cPanel) Instructions

---

## ✅ PRE-FLIGHT CHECKLIST

Before deploying, confirm:
- [ ] Google Analytics ID `G-HXFNEEB0BX` is on every page (already done)
- [ ] All placeholder codes removed (already done)
- [ ] WhatsApp button fixed (already done)
- [ ] Sitemap is up to date (already done)

---

## STEP 1 — Push to GitHub

```bash
# In your local project folder
git init                          # only if not already a repo
git add .
git commit -m "v6 - analytics, mobile fixes, WhatsApp fix"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/pinewood-electrical.git
git push -u origin main
```

> If repo already exists: `git push origin main`

---

## STEP 2 — Deploy to GoDaddy (cPanel File Manager)

### Option A — Manual Upload (Simplest)
1. Log into GoDaddy → **My Products** → **Web Hosting** → **Manage**
2. Open **cPanel** → **File Manager**
3. Navigate to `public_html/`
4. Upload ALL files and the `static/` folder
5. Make sure `index.html` is directly inside `public_html/` (not in a subfolder)

### Option B — cPanel Git Version Control (Recommended)
1. In cPanel, search for **Git Version Control**
2. Click **Create** → enter your GitHub repo URL
3. Set **Repository Path** to `/home/USERNAME/public_html`
4. Clone → then use **Pull or Deploy** on each update

---

## STEP 3 — File Structure in public_html

```
public_html/
├── index.html          ← homepage
├── about.html
├── services.html
├── contact.html
├── faq.html
├── reviews.html
├── industries.html
├── ev-charger.html
├── electrical-upgrades.html
├── control-panels.html
├── maintenance.html
├── plc-automation.html
├── residential.html
├── sitemap.xml
├── robots.txt
└── static/
    └── main/
        ├── style.css
        ├── app.js
        └── images/
```

---

## STEP 4 — After Deployment Checklist

- [ ] Visit https://www.pinewoodelectrical.ca — homepage loads
- [ ] Check navigation on mobile (hamburger menu works)
- [ ] WhatsApp button is small and fixed (bottom-right, not full screen)
- [ ] Sticky "Call Now" bar appears on mobile at bottom
- [ ] All internal links work (no 404s)
- [ ] Open GA4 → Real-Time → visit site → confirm active users shows up

---

## STEP 5 — Google Analytics Verification

1. Go to https://analytics.google.com
2. Select your property
3. Go to **Reports** → **Real-time**
4. Open your website in another tab
5. Confirm you see yourself as an active user

**Your GA4 ID:** `G-HXFNEEB0BX`

---

## STEP 6 — Google Search Console (Optional but Recommended)

1. Go to https://search.google.com/search-console
2. Add property: `https://www.pinewoodelectrical.ca`
3. Verify via GA4 (automatic if same Google account)
4. Submit sitemap: `https://www.pinewoodelectrical.ca/sitemap.xml`

---

## TRACKED EVENTS (GA4)

These fire automatically — view them in GA4 → Events:

| Event Name        | Triggers When                        |
|-------------------|--------------------------------------|
| `phone_click`     | Any `tel:` link clicked              |
| `email_click`     | Any `mailto:` link clicked           |
| `whatsapp_click`  | WhatsApp button clicked              |
| `sticky_call_click` | Mobile sticky call bar clicked     |
| `cta_click`       | Gold CTA buttons clicked             |
| `form_submit`     | Contact/quote form submitted         |

