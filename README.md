# Ritesh Shah Auto Point (I) – Next.js website + admin

Used-car dealer site with a password-protected admin panel (`/admin`). Ready for Vercel.

## Deploy on Vercel (about 5 minutes)
1. Upload this folder to a GitHub repo.
2. Vercel -> **Add New Project** -> import the repo.
3. In the project, open **Storage** -> **Create** -> **Blob** -> connect it to the project
   (this adds `BLOB_READ_WRITE_TOKEN` automatically).
4. **Settings -> Environment Variables**: add `ADMIN_PASSWORD` (your password) and
   `SESSION_SECRET` (any long random text).
5. **Deploy** (or Redeploy after adding the variables). Open `your-site.vercel.app/admin`.

## Edit from /admin
Shop name, phones, WhatsApp, location, timings, hero text, stats, about, delivery updates and steps,
cars (details, photos, mark as SOLD). Press **Save** – it goes live instantly.
Photos are auto-resized before upload.

## Run locally
`npm install` -> copy `.env.example` to `.env.local` -> `npm run dev`.
Without a Blob token, local edits are saved in `data/content.local.json` and `data/uploads/`.

## Notes
- Default content: `data/content.json`. Logo: `public/logo.jpg`.
- The password lives only in environment variables, never in the browser.
- The site is installable on phones (PWA manifest + icons included).
