# ScanSetU LP Landing Page v2

## Included
- ScanSetU-style dark, modern landing page based on the public site's visual/content direction.
- LP explanation and rewards sections.
- Realistic partner-desk interaction:
  1. Received Buy Order — order ID + amount + small received notification + slide to confirm.
  2. Send Order — order ID + QR/UPI payment instruction, no wallet address shown + slide to confirm.
  3. Scan & Pay — order ID + realistic non-functional QR + scan-success notification + payment-success notification + slide to confirm.
  4. Earnings — total example commission + wallet withdrawal preview.
- Application form with ONLY Name, Telegram ID and Email.
- “Team will connect with you” message.
- Official public social links: Telegram @scansetuapp, X @scansetupay, Instagram @scansetupay.
- Responsive mobile layout.

## Run locally
Open index.html directly, or:
python3 -m http.server 8080
Then open http://localhost:8080

## Deploy
### Vercel
1. Create a GitHub repository.
2. Upload index.html.
3. Import the repository into Vercel.
4. Deploy.
5. Add scansetu.co/lp (or your chosen subdomain/path) in Domains/DNS.

### Netlify
Drag the folder to Netlify's manual deploy area, or connect the GitHub repository.

## Production changes required
This is a front-end interaction preview. Before connecting it to real LP operations:
- Move order state and commission calculations to the server.
- Create real authenticated LP sessions.
- Pull live order IDs, amounts, status and payment instructions from the backend.
- Verify incoming payments server-side before allowing confirmation.
- Never expose a real wallet/private key/seed phrase in front-end code.
- Use a real payment/QR provider only for the production transaction flow.
- Connect application form to CRM/API.
- Add consent/privacy handling and rate limiting.
- Keep promotional rate/reward rules configurable server-side.
