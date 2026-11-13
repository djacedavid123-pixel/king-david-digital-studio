# King David Digital Studio

The current website, ready for GitHub and Render. It is a static site, not a Node or Python application. No npm install, build framework, start command, backend, database, or secrets are required.

## Repository structure

```text
public/
  index.html
  favicon.ico
  robots.txt
render.yaml
README.md
.gitignore
```

`public/index.html` contains the website, embedded logo images, CSS, scripts, orbital word sphere, and WebGL scan. Only the `public` folder should be published.

## 1. Upload to GitHub

1. Sign in at https://github.com and create a repository called `king-david-digital-studio` (or use a name you prefer).
2. Extract the ZIP on your computer. Upload its CONTENTS, preserving the `public` folder. Do not upload the ZIP itself and do not add an extra enclosing folder.
3. Commit the files to the `main` branch. At the repository root, you should see `public`, `render.yaml`, and this README.
4. Public or private is your choice; authorize Render to access this repository. A public repository exposes the source code. No secrets are included in this package.

## 2. Publish on Render — recommended Blueprint path

1. Sign in at https://dashboard.render.com.
2. Choose **New > Blueprint**, connect GitHub, and select your repository.
3. Select the `main` branch. Keep the Blueprint file path as `render.yaml`.
4. Review the proposed static site and any billing information, then confirm deployment.
5. When deployment succeeds, open the actual public URL shown by Render. The final URL is assigned by Render; no URL has been reserved by this package.

The Blueprint sets the publish directory and basic response headers. It also disables camera, microphone, and geolocation permissions; none are required by this website.

## Alternative: manual Static Site setup

If you use **New > Static Site** instead of Blueprint, enter:

| Setting | Value |
| --- | --- |
| Repository | The GitHub repository you uploaded |
| Branch | `main` |
| Root Directory | Leave blank |
| Build Command | `echo "Static website ready"` |
| Publish Directory | `public` |
| Environment variable | `SKIP_INSTALL_DEPS=true` |

Do NOT select Web Service and do NOT enter a Python server or npm start command. Manual creation does not automatically apply the headers in `render.yaml`; add those under the site's Headers settings if using this path.

## 3. Verify after deployment

- Open the public HTTPS URL in a fresh browser tab. The 4.5-second opening plays once per tab session (unless reduced motion is enabled).
- Confirm the logo and orbital word sphere appear. Left-click the sphere to spin; proximity tilt and repeated-click acceleration are enabled, with no visible usage instructions.
- Test a phone-sized view and reduced-motion settings.
- Confirm Start a project reveals the hidden enquiry form.
- Confirm email links and Copy use `kingdaviddigitalstudio@gmail.com`.
- Confirm WhatsApp links point to `+234 902 862 8633`.
- Test the form: it prepares a WhatsApp message and opens WhatsApp; the visitor still needs to send it.
- Verify the concept showcase is labelled as fictional concepts, not client commissions.

## Before sharing publicly

Review all company copy, concept examples, and the enquiry privacy notice. Confirm the contact details are correct and that the privacy text matches your actual handling and retention of enquiries. The notice is implementation-focused, not a certification of legal compliance.

Google Fonts requires an external network request. System fonts provide a fallback. The WebGL effect has a Canvas fallback. There is no webcam access, analytics script, advertising script, payment processing, or form backend in the page.

## Updates

Update `public/index.html` and commit to the branch Render deploys. Ensure automatic deploys are enabled in your Render settings, or trigger a manual deploy after a commit.

## Custom domain

Once the generated Render URL works, add your domain in the site's Settings and use the exact DNS records Render provides. Do not guess DNS targets. After selecting a permanent domain, add a matching canonical URL, social-share metadata, and sitemap as a follow-up.

## Local preview (optional)

From this repository's root:

```sh
python3 -m http.server 8000 --directory public
```

Then visit http://localhost:8000. This command is only for local preview, not the Render deployment.

## Official deployment references

- https://render.com/docs/static-sites
- https://render.com/docs/blueprint-spec

Deployment package prepared 12 November 2026. This package is ready to upload; it has not been pushed to GitHub or published to Render automatically.
