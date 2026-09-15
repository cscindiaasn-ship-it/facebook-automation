# Facebook Page publishing checklist

1. Create/configure a Meta developer app and add the products/permissions required for your intended Facebook Page publishing use case.
2. Identify the Facebook Page ID for the Page you control.
3. Obtain a valid Page access token using Meta's supported authentication flow for your app/Page.
4. Store the token as an n8n secret/environment variable; do not put it in GitHub.
5. Test the Graph API call against your own Page with a harmless message before enabling scheduled publishing.
6. Review Meta's current documentation for the exact permissions, review requirements, token behavior, and Graph API version applicable to your app because these can change.

The workflow in this repository uses a Page `/feed` publishing request and reads the Page ID/token from n8n environment variables. Do not copy real tokens into workflow JSON.
