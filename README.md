# Canvas Assignment Scanner (GitHub Pages)

A static, read-only browser app for scanning courses and assignments from your own Canvas account.

## Publish with GitHub Pages

1. Create a **new private GitHub repository** if your GitHub account and school policy allow it. The page itself can be public, but a private repository is preferable for source management.
2. Upload `index.html` to the repository's root (the top level, not inside another folder).
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose branch `main` and folder `/ (root)`, then save.
6. Wait for GitHub Pages to publish. Open the Pages URL shown in Settings → Pages.

If GitHub Pages is blocked or your school does not permit publishing this kind of tool, stop and ask school IT or your teacher for an approved route.

## Use

1. Open the published page.
2. Confirm the Canvas site is `https://4j.instructure.com`.
3. Paste your Canvas API token into the password field and select a scan scope.
4. Click **Scan Canvas**.
5. Export JSON or CSV when the scan completes.
6. Clear the token and results when finished, then close the tab.

## Security

- Never put a Canvas token in this repository, source code, URL, issue, screenshot, or exported file.
- The app does not use localStorage, cookies, analytics, external libraries, or a third-party proxy.
- The token exists in the page's memory while the tab is open and is sent directly to the Canvas site in API request headers.
- Use only a token you are authorized to create and use. Revoke it in Canvas when finished.
- Do not use this on a shared device. Follow school rules and ask school IT/your teacher if unsure.

## Limitations

- The Canvas server must permit browser cross-origin (CORS) API requests from the GitHub Pages origin. If it does not, the browser blocks the request; this app cannot and does not bypass that control.
- A course or assignment that your Canvas account cannot access will not be included.
- The app reads data only. It does not submit assignments, edit grades, or change course settings.
