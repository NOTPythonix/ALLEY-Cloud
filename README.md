# ALLEY Cloud website concept

Responsive static website concept for a service combining Gemini-powered AI, secure access to a home Raspberry Pi, and personal website/domain hosting. Uses the ALLEY Cloud logo supplied by the project owner.

## Included pages

- `index.html` — home page, feature overview, interactive-looking demo previews, and Free / Plus ($5/month) / Pro ($10/month) / Ultra ($25/month) / Business (custom) plan cards.
- `auth-required.html` — account-required page reached by plan and gated feature actions; offers sign up or log in while preserving the plan/feature selection.
- `signup.html` — sign-up form for the front-end demo.
- `login.html` — login form for the front-end demo.
- `account.html` — sample account dashboard.
- `assets/` — logos, styles and JavaScript.

## Test locally

Open `index.html` in a modern browser. All subpages and assets should stay in the same project folder. To test end-to-end navigation, click a plan or a gated feature, create a demo account, and inspect the account dashboard. The mock sign-in uses `sessionStorage` only to demonstrate navigation. It does not provide authentication or security.

## Publish a temporary public test URL

1. Open https://app.netlify.com/drop .
2. Upload the **contents of this project folder** (or upload the ZIP if the page accepts it). Keep `index.html` at the top level, with `auth-required.html`, `signup.html`, `login.html`, `account.html`, and the `assets/` folder beside it.
3. Netlify will provide a public `*.netlify.app` preview URL after deployment. The exact address is assigned by the host, so it cannot be known before you publish. See https://docs.netlify.com/start/quickstarts/netlify-drop-quickstart/ .

## Important: front-end prototype only

The AI chat uses sample scripted responses and does not call Google Gemini. The terminal is simulated and never SSHes into a Raspberry Pi. The signup/login pages do not create real accounts; they do not send or save passwords, and the demo session is not secure. The chosen plan is not purchased or activated. There is no payment processing, persistent user database, custom-domain registration/DNS, secure remote-access tunnel, or real website hosting. Do not use real credentials on the demo.

Before public launch, implement server-side authentication and session management, account storage, Gemini API calls using server-side secrets, secure Pi enrollment and SSH/tunnel access, payment processing, usage entitlements, abuse protection, domain DNS/TLS, site isolation, and hosting provisioning. Never put a production Gemini API key or SSH private key into public browser code.
