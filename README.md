# Security Header Analyzer

A dependency-free browser tool for reviewing common HTTP response security headers.

## Features

- Analyzes CSP, HSTS, MIME sniffing, framing, referrer, and permissions policies
- Gives a 0–100% baseline security score
- Uses light and dark themes from system preferences
- Saves the last pasted headers in localStorage
- Runs locally with no server or installation

## Run locally

1. Clone the repository.
2. Open `index.html` in a modern web browser.

For browser development tools, open the Network tab, select a response, and copy its response headers into the text area.

## Scope

This tool provides an introductory header review, not a complete security assessment. Header presence alone does not establish that a policy is safe or effective.
