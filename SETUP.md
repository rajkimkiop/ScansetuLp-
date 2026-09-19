# ScanSetU LP Landing Page + Interactive Demo

## What is included
- Modern responsive LP landing page
- 3-step interactive demo:
  1. Received Buy Order -> Confirm Received
  2. Send Order -> Send & Complete
  3. Scan & Pay Order -> Complete
- 2.5% example commission after each completed demo order
- Final total demo earning screen
- LP application form
- FAQ, rewards, contact and risk-disclosure sections

## Important
The demo is front-end only. It does NOT:
- connect to a wallet
- broadcast USDT
- process a real UPI payment
- create a real order
- calculate live commission
- submit the application to a server

Before production, connect the form and demo to your real backend/API and replace placeholder support details.

## Local test
Open index.html in a browser, or run:
python3 -m http.server 8080
Then visit http://localhost:8080

## Vercel
1. Put this folder in a GitHub repository.
2. In Vercel, create a New Project and import the repository.
3. Deploy.
4. Add your domain in Project Settings -> Domains.

## Netlify
1. Sign in to Netlify.
2. Add new project / Deploy manually.
3. Drag this folder (or its contents) to the deploy area.
4. For ongoing development, connect the Git repository so pushes automatically deploy.

## Production backend checklist
- POST /api/lp/apply
- POST /api/demo/session
- GET /api/demo/order
- POST /api/demo/order/:id/complete
- Server-side commission calculation
- Database for LP leads and demo sessions
- Rate/offer configuration on server, not hard-coded in browser
- Fraud/rate-limit protection
- Admin dashboard
- Analytics: source -> visit -> demo start -> demo completion -> application -> verified -> funded -> first live order
