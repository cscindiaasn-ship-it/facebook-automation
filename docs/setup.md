# Setup

## 1. Import the n8n workflow

Open n8n → Workflows → Import from File and select `n8n/facebook-page-automation.json`.

The workflow is inactive after import. Review every node before activation.

## 2. Configure secrets

Use n8n credentials or the n8n runtime environment for secrets. Never commit API keys, Facebook access tokens, app secrets, passwords, or cookies to GitHub.

Required values:

- `OPENAI_API_KEY`
- `OPENAI_MODEL`
- `FACEBOOK_PAGE_ID`
- `FACEBOOK_PAGE_ACCESS_TOKEN`
- `APPROVAL_EMAIL`
- `NOTIFY_EMAIL`

## 3. Connect Gmail

The approval and notification nodes use Gmail. Create/select your Gmail OAuth2 credential in n8n and replace the placeholder credential reference created by the import.

## 4. Test content generation

Run the workflow manually. Confirm that the AI output contains `title`, `caption`, and `hashtags` JSON fields and that the Hindi text is accurate.

## 5. Test approval

Use the approval email and choose Publish or Reject. Keep approval enabled while testing.

## 6. Test Facebook publishing

Before activating the schedule, test with a Page you control and a harmless draft. Confirm the Page ID and Page access token are valid and that the Page is authorized for the intended publishing operation.

## 7. Activate

After successful manual testing, activate the workflow. The schedule is configured for 09:00 in `Asia/Kolkata`.

## Recommended production additions

- Google Sheets or a database for the content queue and publication log.
- A separate retry/error workflow.
- A daily duplicate-content check.
- A content review rule for legal/government claims.
- Image generation/storage as a separate step before approval.
