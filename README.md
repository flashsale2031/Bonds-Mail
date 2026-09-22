# Bonds Mail

Bonds Mail is a responsive, Outlook-inspired email interface built with HTML, CSS, JavaScript and PHP.

## Requested mailbox modules

- `index.html` — main Bonds Mail UI
- `bondsmail.js` — shared JavaScript functions, local state and PHP synchronization
- `inbox.html`, `inbox.js`, `inbox.php` — inbound messages
- `outbound.html`, `outbound.js`, `outbound.php` — compose/outbound messages
- `sent.html`, `sent.js`, `sent.php` — sent messages
- `drafts.html`, `drafts.js`, `drafts.php` — drafts
- `promotions.html`, `promotions.js`, `promotions.php` — promotional messages
- `promotions.PHP` — compatibility filename requested for the promotional PHP module
- `favorites.html`, `favorites.js` — favorites
- `allmail.html`, `allmail.js`, `allmail.php` — all mail
- `spam.html`, `spam.js`, `spam.php` — spam
- `trash.html`, `trash.js`, `trash.php` — trash
- `bondsmail.css` — shared responsive UI

## Hosting

The frontend can be hosted from a GitHub repository or GitHub Pages. GitHub Pages does **not** execute PHP. Bonds Mail therefore keeps a browser localStorage data layer for static hosting while the JavaScript attempts to synchronize with the PHP endpoints when the application is deployed on a PHP-capable server.

For server-backed email, deploy the PHP files to a PHP-capable host and provide a writable `data/` directory.

## Production requirements

The included PHP endpoints are a functional foundation, not a complete public email service. Production deployment should add authenticated accounts, SMTP/IMAP integration, a database, authorization checks, CSRF protection, rate limiting, input validation, secure attachment handling, and server-side message persistence.
