# Facebook Automation with n8n

Hindi-first Facebook Page content automation for a CSC/deed-writer information page.

## Flow

`Schedule Trigger → Generate Content → Validate → Approval Gate → Publish to Facebook Page → Log Result`

The default design keeps **human approval enabled**. Credentials and Page tokens are never stored in this repository.

## Repository structure

- `n8n/facebook-page-automation.json` — importable starter workflow
- `prompts/content-generator.txt` — Hindi post prompt
- `prompts/image-generator.txt` — image prompt
- `prompts/rewrite.txt` — rewrite prompt
- `google-sheets/sheet-structure.csv` — recommended sheet columns
- `config/.env.example` — configuration placeholder names
- `docs/setup.md` — setup checklist
- `docs/facebook-page-api.md` — Facebook Page API checklist
- `docs/n8n-import.md` — n8n import/configuration guide

## Important

Replace placeholder values with your own n8n credentials/environment variables. Do not commit access tokens, app secrets, API keys, cookies, or passwords.

This automation is intended for a Facebook **Page**, not a personal profile, and should be used for legitimate, non-spam publishing.
