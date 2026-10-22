# Human Group warehouse recruitment landing page

A dependency-free, mobile-first landing page in Ukrainian, Polish, English, Spanish and Russian.

## Local preview

```sh
cd /workspace/Lending-dla-kampanii-zewntrznej-
python3 -m http.server 8080
```

Open `http://localhost:8080` locally. The form deliberately refuses to report success until `leadEndpoint` in `config.js` points to a secured same-origin POST handler that stores or forwards leads. That handler must validate input server-side, limit abuse, protect recruiter credentials, and return a 2xx response only after successful delivery. The client sends name, phone, messenger, location, consent, UTM fields, page path and submission time. A successful response triggers the `generate_lead` event.

Before a public launch, fill in verified business details, contact links and analytics IDs in `config.js`, and replace the placeholder privacy policy and terms with approved legal text. The `leadEndpoint` must not expose a Telegram bot token in browser code. The site's claims about pay, housing and benefits come from the supplied brief and require business verification.

This is a static website. A public URL requires hosting or deployment; local preview URLs cannot be shared externally.
