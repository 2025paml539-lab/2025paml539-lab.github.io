# Kishore Nandhaluru – Portfolio & Demo Apps: Work Log

Tracking document for everything built and changed in this project.

- **Live site:** https://2025paml539-lab.github.io
- **GitHub repo:** https://github.com/2025paml539-lab/2025paml539-lab.github.io
- **Local repo (main copy):** `D:\portfolio-site`
- **Build/helper files:** `D:\BITS\build` (scripts, screenshots, resume source)

---

## 1. Portfolio profile page (`index.html`)

### Fixes to the original page
- Embedded the profile photo inside the HTML (resized JPEG, about 70 KB), so it shows from any folder or host.
- Embedded the resume as a PDF inside the HTML. Every "Resume / Download resume" button downloads `Nandhaluru Kishore - Resume.pdf`, with no extra files needed.
- Fixed reduced-motion bug (sections stuck shifted sideways).
- Content now shows if JavaScript is off; stats show real values instead of "0".
- Contact grid layout fixed (Location box centred).
- Award badge "IRMS" replaced with "Boeing".
- Added favicon, theme colour and link-preview (Open Graph) tags.

### Content changes
- Removed "Open to lead & architect roles" pill (not job hunting).
- Tagline changed to "I build & modernize **enterprise software & AI solutions** that fly."
- Intro and badge broadened beyond .NET ("9+ yrs engineering", Python, AI/ML).
- Contact line changed to: web, mobile and AI projects; freelance and consulting enquiries welcome.

### Layout
- Header: name and title on one line each; nav folds into ☰ menu below 1180px.
- Fully responsive: tested at 320, 375, 768, 1100 and 1440px widths, plus phone landscape.
- Fixed "99%+ uptime" badge being cut off next to the photo.

### Chat assistant (bottom-left round button)
- Speech-bubble icon that turns into an X when open; red "1" badge; gentle bounce and "See my work 👋" tooltip until first opened.
- Panel pops open with a spring animation; closes on the X, Esc, or tapping outside.
- Greeting shows all six demo cards.
- Quick replies: Show me your work, What can you build, Mobile apps, AI & ML, Contact / hire, Download resume.
- Typed questions matched by keyword (aerospace, retail, healthcare, diagnostics/MRI, payroll/salary, bakery/cake, price, resume...).
- Scripted assistant, not real AI. Pricing questions point to WhatsApp.

---

## 2. Demo apps (all fictional data, single HTML file each)

Common to all: works offline, phone/tablet/desktop layouts, light/dark toggle, "Demo data" badge, "Reset demo data", WhatsApp/Email/Portfolio buttons, installable as a phone app (PWA).

| Demo | File / URL | Highlights |
|---|---|---|
| **SkyOps MRO** (aerospace) | `aerospace-mro.html` | 24-aircraft fleet, AOG command center with live ground-time clocks and 6-stage workflow, Raise AOG, hangar Gantt schedule, work orders with MEL countdowns, parts expedite/receive, AD/SB compliance, life-limited parts |
| **ShopPulse** (retail) | `retail-store.html` | Sales dashboard, POS billing with GST, coupons and loyalty lookup (try 98450 11223), printable receipt, 3-store inventory, orders with status flow and returns, coupon creation, customer storefront |
| **CareSync** (healthcare) | `healthcare-clinic.html` | Appointment booking by doctor/date, patient records with vitals chart, record vitals, pharmacy expiry alerts, lab orders, billing with insurance claims, ER triage queue, ward beds, mock video consultation |
| **LifeScan Diagnostics** | `diagnostics-center.html` | About 170 pathology, radiology (X-ray, USG, CT, MRI, mammography, PET) and cardio/neuro tests with cost, prep and report time; 7 health packages; coupon LIFE10; booking with home collection; machine slot board; worklist; downloadable lab/radiology reports |
| **PayDesk Payroll** | `payroll-system.html` | 30 employees incl. ₹20 LPA package; salary structure sliders; old vs new regime tax calculator (FY 2025-26 slabs); payroll run (compute → approve → disburse); payslip PDF with net pay in words and YTD; 8 reports with CSV (salary register, PF ECR, ESI, PT, TDS 24Q, bank advice, dept cost, month-on-month) |
| **Golden Crust Bakery** | `bakery-shop.html` | About 40 Bengaluru bakery items with prices (dilpasand, khara bun, egg puff, honey cake...), live cake designer, cart with delivery areas, WhatsApp order; **Owner login PIN 1234**: add items with photo upload, edit prices, sold out, bestseller, today's special, order board |

Supporting files: `manifest-*.json`, `sw.js` (offline cache), `icons/`.

### Latest styling pass
- Dashboards moved to flat, industry-matched light themes with dark sidebars:
  - Aerospace: navy and amber
  - Retail: cream and coral
  - Healthcare: white and teal
  - Diagnostics: white and indigo
  - Payroll: cream and ledger green
- Fixed mobile/tablet sidebar links not being tappable (overlay was on top of the menu).

---

## 3. Hosting

- GitHub Pages, branch `main`, folder `/ (root)`.
- To update: edit files in `D:\portfolio-site`, then:
  ```
  git add -A
  git commit -m "Describe the change"
  git push
  ```
  The site refreshes 1 to 2 minutes later (Ctrl+F5 to bypass cache).

---

## 4. Known gaps / to check

- Diagnostics and bakery prices are realistic estimates, not verified live Bengaluru prices. Review before showing a real client.
- Tax calculator is indicative: marginal relief on surcharge is not modelled.
- Mobile sidebar fix and latest chat changes were not tested on a real phone.
- The page publishes your phone number and Boeing/client project details. Check this is fine with your employer's confidentiality policy.
- Resume title ("Senior Full Stack Software Engineer") differs from the profile title ("Lead Technical Senior Software Engineer").
- Resume PDF is fixed at build time. To change it, edit `D:\BITS\build\resume.html` and rebuild.

## 5. Ideas not yet built
- QR code for each demo URL.
- "Live demos" section on the profile page.
- Kannada/Hindi labels.
- Custom domain.
