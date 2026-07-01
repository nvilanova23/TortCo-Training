# Tort Co Encryption & Data Protection Course

Static interactive eLearning course designed for GitHub and Cloudflare Pages.

## Deploy with Cloudflare Pages

1. Upload this entire `cloudflare-course` folder to a GitHub repository.
2. In Cloudflare, open **Workers & Pages** and choose **Create > Pages > Connect to Git**.
3. Select the GitHub repository.
4. Use these build settings:
   - Framework preset: `None`
   - Build command: leave blank
   - Build output directory: `public`
5. Select **Save and Deploy**.

No environment variables, database, or server are required.

## Completion tracking

Progress and quiz results are stored in the learner's browser using `localStorage`.
After passing the quiz, the learner can download a JSON completion record.
For centralized employee reporting, connect the completion event in `app.js` to an LMS, Cloudflare Worker, D1 database, or analytics endpoint.

## Local preview

From this folder, run:

```powershell
npx serve public
```

Then open the displayed local address.
