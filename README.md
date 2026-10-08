# InceptionApps

Small, focused developer tools for macOS, iOS and Android — built by [@nhrclk](https://github.com/nhrclk).

---

## Apps

### 🎭 Mock Easy — local mock and proxy server for macOS

Point Mock Easy at your real API, click **Record**, and every response becomes a reusable mock. Turn **Intercept** on to pause any request mid-flight and rewrite the JSON before it reaches your client. Multiple routes on their own ports, live log with a searchable JSON tree, HTTPS out of the box.

*Free on the Mac App Store.* The free version includes one route, five endpoints, mocks, HTTPS and the live log. **Mock Easy Pro** (monthly or yearly, first month free) adds unlimited routes and endpoints, proxy, recording, intercept, and import/export. Bought Mock Easy 1.0? Pro is already yours, for good.

**Common questions**

- **The self-signed HTTPS certificate isn't trusted by my client**  
  In the app, click **🔒 Cert** in the top-right → **Download cert**. Install it in the trust store of the machine or device that will call your mock ports.
  - macOS: double-click and mark the cert as trusted for SSL in Keychain Access.
  - Android emulator: drag the file in, then Settings → Security → Install from storage. Debug builds may also need a `network_security_config.xml` that trusts user CAs.
  - iOS simulator: drag the file onto the simulator, install via Settings, and enable it under Certificate Trust Settings.

- **Recording is on but no endpoints are being captured**  
  Recording only captures 2xx responses that were proxied through the route. Make sure both **Proxy** and **Recording** are enabled on that specific route (per-route toggles, not just the global header pill).

- **My OkHttp/Retrofit client refuses to talk to Mock Easy over HTTPS**  
  If the client uses SSL pinning (BKS truststore or `CertificatePinner`), it will reject the self-signed cert. Either add Mock Easy's cert to that trust store, or bypass pinning in your debug flavour only.

- **Client hits the route port and gets `connection refused`**  
  That port doesn't have a route bound to it — check the Routes drawer, confirm the port number, and make sure the route is enabled.

- **How do I cancel or change my Pro subscription?**  
  Subscriptions are managed by Apple: open the App Store app → click your name → **Account Settings** → **Subscriptions**, or click **★ Pro** in Mock Easy → **Manage Subscription**. Cancel at least 24 hours before the renewal date to avoid the next charge; you keep Pro until the end of the period you paid for.

- **I'm subscribed (or I bought 1.0) but the app shows the free version**  
  Click **★ Go Pro** → **Restore Purchases** and sign in with the Apple Account you bought with. The first check after an update needs an internet connection.

- **Do you collect any data?**  
  No. Mock Easy is fully sandboxed, has no telemetry, no analytics, no cloud login. Your endpoints, configs, and captured responses live only on your Mac.

---

## Support & feedback

Email: **[inceptionapplication@gmail.com](mailto:inceptionapplication@gmail.com)**  
Or open a [GitHub Issue](https://github.com/nhrclk/inceptionapps/issues/new).

Replies usually within a couple of days.

---

## Privacy

We collect nothing. No accounts, no telemetry, no analytics — everything the app produces stays on your device. Full policy: [PRIVACY.md](PRIVACY.md).

## About

InceptionApps is a small independent studio making desktop and mobile tools that stay out of your way. No accounts, no lock-in, no upsells.
