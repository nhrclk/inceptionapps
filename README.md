# InceptionApps

Small, focused developer tools for macOS, iOS and Android — built by [@nhrclk](https://github.com/nhrclk).

---

## Apps

### 🎭 Mock Easy — local mock and proxy server for macOS

Point Mock Easy at your real API, click **Record**, and every response becomes a reusable mock. Turn **Intercept** on to pause any request mid-flight and rewrite the JSON before it reaches your client. Multiple routes on their own ports, live log with a searchable JSON tree, HTTPS out of the box.

*Available on the Mac App Store.*

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

- **Do you collect any data?**  
  No. Mock Easy is fully sandboxed, has no telemetry, no analytics, no cloud login. Your endpoints, configs, and captured responses live only on your Mac.

---

## Support & feedback

Email: **[inceptionapplication@gmail.com](mailto:inceptionapplication@gmail.com)**  
Or open a [GitHub Issue](https://github.com/nhrclk/inceptionapps/issues/new).

Replies usually within a couple of days.

---

## About

InceptionApps is a small independent studio making desktop and mobile tools that stay out of your way. No accounts, no lock-in, no upsells.
