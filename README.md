# SecureSign — Type-C DSC Mobile Signing

A generic, vendor-agnostic middleware + SDK that lets **any** mobile app (Android & iOS)
sign documents using a **Type-C DSC dongle** — matching the plug-and-play experience of
desktop DSC signing, fully compliant with CCA (Controller of Certifying Authorities) guidelines.

> Built for the **SecureSign Innovation Challenge** (NIC AP + APTS + Ratan Tata Innovation Hub).
> Submission deadline: **07 Jul 2026** · Demo/Pitch: **15 Jul 2026**

---

## The one-sentence pitch

> Desktop DSC signing is plug-and-play. On mobile it's impossible — because every DSC token
> in India ships with a USB-A plug and phones don't have that port. SecureSign is the software
> layer that makes USB-C DSC tokens sign documents inside any mobile app or mobile web view,
> on Android and iOS, for any CCA-licensed token vendor.

## Why we win this

- **We have lived the problem.** We procured Class 3 org + individual director DSCs through
  eMudhra / PantaSign during Devit's incorporation. We know the PKCS#11 handshake, the PIN
  flow, the CCA certificate chain — not from Googling, from doing it.
- **Vendor-agnostic by design.** All Indian DSC tokens speak the same CCID + PKCS#11 protocol
  underneath. Our SDK works with eMudhra, PantaSign, Capricorn, nCode, ProDigiSign — no
  per-vendor code. That's 10 marks on Interoperability the others will fudge.
- **Intellectual honesty on iOS.** We don't fake the hard part. We ship a working Android
  solution + a credible, sourced iOS architecture. Judges respect that over vapourware.

## Repository layout

```
securesign/
├── README.md                  ← you are here
├── docs/
│   ├── 00_MASTERPLAN.md       ← strategy, roadmap, money model, inputs/outputs/cost
│   ├── 01_ARCHITECTURE.md     ← technical architecture (Android + iOS tracks)
│   ├── 02_CCA_COMPLIANCE.md   ← CCA-IOG compliance mapping (the shortlisting gate)
│   └── 03_BUILD_PLAN.md       ← day-by-day build plan against the real deadlines
├── android-sdk/               ← the core product: Kotlin SDK (.aar), USB CCID + signing
├── webview-bridge/            ← JS bridge — one-line signing API for any web view
├── demo-app/                  ← live PDF-signing demo for pitch day
├── ios-design/                ← iOS architecture doc (CryptoTokenKit + BLE bridge)
└── submission/                ← concept note, compliance table, pitch deck
```

## Status

| Component            | State        | Details |
|----------------------|--------------|---------|
| Strategy & docs      | ✅ Completed | Masterplan, CCA Compliance mapping, Runbooks |
| Android USB CCID     | ✅ Completed | Native Kotlin CCID / APDU transport Layer |
| ePass2003 On-Device  | ✅ Completed | Direct on-phone signing under SCP01 secure messaging |
| WebView JS bridge    | ✅ Completed | JS shim + `@JavascriptInterface` bridge |
| Demo app             | ✅ Completed | Material 3 Android App with native / WebView tabs |
| iOS architecture doc | ✅ Completed | Sourced `CryptoTokenKit` design specifications |
| Submission package   | ✅ Completed | Concept Note, Tech Arch, Presentation PDFs generated |

---

## 🔒 Source Code Access

To protect intellectual property, this public repository contains only the documentation, screenshots, and submission assets. The full implementation, including the Android SDK source code, compiled libraries, and bridge middleware, is hosted in a private repository. 

Access is readily available to the **APTS/NIC evaluation committee** upon request:

*   🟢 **[Contact via WhatsApp](https://wa.me/919553321211?text=Hello%21%20I%20would%20like%20to%20request%20access%20to%20the%20SecureSign%20SDK%20private%20repository.)** (Direct chat link for mobile)
*   ✉️ **[Request Access via Email](mailto:workwithdevit@gmail.com?subject=Request%20Access%20to%20SecureSign%20SDK%20Repository&body=Hello%20WEDEVIT%20Team%2C%0A%0AWe%20are%20members%20of%20the%20SecureSign%20Innovation%20Challenge%20evaluation%20committee.%20We%20would%20like%20to%20request%20access%20to%20the%20private%20repository%20containing%20the%20source%20code%20and%20SDK%20libraries.%0A%0ARegards%2C%0A%5BName%5D)** (Pre-filled template)
