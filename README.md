# Security Header Analyzer

A dependency-free browser tool for reviewing common HTTP response security headers.

## Features

- Analyzes CSP, HSTS, MIME sniffing, framing, referrer, and permissions policies
- Gives a 0–100% baseline security score
- Uses light and dark themes from system preferences
- Saves the last pasted headers in localStorage
- Runs locally with no server or installation

## Run locally

1. Clone the repository:
   ```bash
   git clone https://github.com/Junaidsheik/security-header-analyzer.git
   ```
2. Open the project directory:
   ```bash
   cd security-header-analyzer
   ```
3. Open `index.html` in a modern web browser.

No installation or build step is required.

## How to use

1. Open the website you want to inspect in a browser.
2. Open browser developer tools and select the **Network** tab.
3. Refresh the page and choose the main document or another response.
4. Open the response-headers section.
5. Copy the response headers, including header names and values, into the app.
6. Select **Analyze headers**.

The analyzer shows a baseline score and reports whether each supported header is present, strong, missing, or worth reviewing.

### Example input

```text
HTTP/1.1 200 OK
Content-Security-Policy: default-src 'self'
Strict-Transport-Security: max-age=31536000; includeSubDomains
X-Content-Type-Options: nosniff
X-Frame-Options: DENY
Referrer-Policy: strict-origin-when-cross-origin
Permissions-Policy: camera=(), geolocation=(), microphone=()
```

The app can also parse only a list of header lines. Header names and values must use the format `Header-Name: value`.

### Reading the results

- **Present, Strong, Enabled, or Configured** indicates a good baseline.
- **Missing** indicates that a recommended header is absent.
- **Review** or **Too short** indicates that the value may need improvement.
- The percentage is an introductory score, not a full security certification.

## Scope

This tool provides an introductory header review, not a complete security assessment. Header presence alone does not establish that a policy is safe or effective.
