# CloudLab Free

A cloud-console learning simulator in a single HTML file. Practise cloud basics (compute, storage, networking, databases, monitoring and billing), take courses, pass labs and earn certificates, all in your browser.

Everything runs locally. There is no server, no database and no real payment. Your progress is saved in your browser's `localStorage`.

**Live version:** https://maruthio5.github.io/CloudLab-free/

## Quick start

Open the live version above, or run it yourself:

1. Download `index.html`.
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari). No install or build step.
3. Choose **Create Free Account** or **Explore Console** (guest mode).

## Features

| Area | What you can do |
|---|---|
| **Account signup** | 7-step flow: account details, phone verification with a one-time code, card check with a ₹1 temporary charge, support plan, and region |
| **Console** | Dashboard, Compute, Networking, Storage, Databases, Observability, Cost, Billing, Account, Notifications |
| **Resources** | Create, start, stop, restart and delete simulated instances, networks, buckets and databases, within free-tier quotas |
| **Courses and labs** | 5 courses with lessons, quizzes, hands-on labs, progress tracking and printable certificates. Take them in any order |
| **Billing** | Checkout with promo codes, transaction history, refunds, invoices (print or CSV), budgets and alerts, payment methods |
| **Extras** | Dark theme, notifications, achievements, keyboard- and screen-reader-friendly layout, mobile layout |

### Courses

1. Cloud Foundations
2. Networking & Databases
3. Security & Monitoring
4. Deploy & Troubleshoot
5. Week 9: Cloud Computing (cloud models, free-account steps, console tour)

Each course is complete when all its lessons are marked done, the quiz is passed (70% or more) and every lab is passed. You can start any course, lesson, quiz or lab at any time. You are enrolled automatically.

## Test data

Use only these sample values.

**Phone:** any made-up number, for example `98765 43210`. The one-time code is shown on screen. No SMS is sent.

**Test cards** (any future expiry, CVV `123`):

| Card number | Result |
|---|---|
| `4242 4242 4242 4242` | Approved |
| `5555 5555 5555 4444` | Approved |
| `4000 0000 0000 0002` | Declined |
| `4000 0000 0000 0119` | Processing error |

**Checkout:** promo codes `LEARN10` (10% off), `SAVE50` (₹50 off), `BUNDLE20` (20% off the bundle). Payment outcome codes: `PAY-SUCCESS`, `PAY-DECLINED`, `PAY-ERROR`.

**Sample sign-in:** username `alex.morgan`, password `learn-cloud`. Or create your own account.

Never enter real card numbers, bank details or passwords. Any card number that isn't one of the test cards above is rejected.

## Admin portal

The admin portal is hidden from the public pages. Open it by adding `#admin` to the page address, or by tapping the logo 5 times quickly.

- Username: `admin`
- Passcode: `learn-admin`
- Roles: Administrator (can override completions and publish courses) or Read-only analyst

It shows the learner account stored in your browser, progress, courses, an audit log and CSV export.

## Reset or erase data

- **Account → Reset data to the sample state** restores the original sample resources.
- **Account → Erase everything** deletes all saved data and signs you out.
- Or clear the site data for the page in your browser settings.

## Limitations

- **Not secure.** The admin passcode is visible in the page source, and lab checks run in the browser, so anyone can edit them. Don't treat this as real access control.
- **Browser-only storage.** Data stays in one browser on one device and is lost if you clear site data.
- **No real services.** There is no email, SMS, database or payment provider. All amounts, invoices and certificates are fictional.
- **Sponsored link.** A labelled, click-only sponsored card appears on the landing page and dashboard. It opens an external site only when you click it.

## Tech notes

- One file: HTML, CSS and vanilla JavaScript, with no external libraries and no network requests on load.
- State is one object saved to `localStorage` (key `cloudlab-free-demo-v1`). The theme is stored separately.
- Passwords are salted and hashed, never stored as plain text.
- The DOM is built with safe helpers (no `innerHTML` for user data).

## Credits

Course content for Week 9 is based on the *IT Skills Week 9* handout (cloud computing, service models, creating a free cloud account, exploring the console).
