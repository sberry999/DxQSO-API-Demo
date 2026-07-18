# DxQSO-API-Demo
DxQSO is a ham radio cloud logbook repository **(It is not a ham radio logbook app!)** which acts as a QSO clearinghouse integrating logbook data from multiple ham radio logbook applications as well as to/from LoTW and QRZ.com and the the DxQSO website and DxQSO mobile applications (Android and IOS).

Through a high speed serverless architecture built on AWS, DxQSO provides a unified view of all logbook data (through a modern API) as well as email and mobile push alerts for new QSLs and new State, DXCC and Grid square QSL achievements. It also includes DxSocial, a social media site built for teams/clubs to share realtime operating QSO data and QSL achievements as well as club based discussions, blogs, files and web links.

The DX-TQSL Windows/Mac application provides realtime DxQSO logbook integration for users whether they use LoTW or not. As a replacement for TQSL, it provides cloud based certificate management and stations and backs up all local TQSL information and uploads to either LoTW and DxQSO or just to DxQSO. 

Users may upload their existing logbooks through the DxQSO website, mobile application or DX-TQSL and maintain all detailed logbook data. When downloaded, Logbook records are automatically converted into target logbook application formats (N1MM, HRD, MacLogger, Polo, etc).

The DxQSO mobile app provides instant access to your entire logbook, real time local logbook updates, QSL alerts for new confirmations, alerts for new QSL Achievements for DXCC, States or Gridsquares and allows you to upload QSOs directly from your mobile via ADIF upload or directly from other mobile apps through the N1MM listener.

**This demo website demonstrates the DxQSO client API which can be used by ham software applications to directly upload ham logbook data, view DxQSO station info and download QSOs.** 

This website is running live on **https://demo.dxqso.net**.

You must have a Vendor Key (Provided by DX Development) and Station Key (provided to DxQSO users for each station they have setup) in order to connect to your DxQSO account data through this demo website.

---

## Repository & deployment

This repository **is** the site served at **https://demo.dxqso.net** — deployed automatically by
Vercel on every push to `main` (no build step; it is static HTML served from the repo root).

- `index.html` — the entire demo (self-contained).
- `vendor/<host>/<path>` — third-party libraries (Bootstrap, jQuery, DataTables, highlight.js,
  JSZip, fonts) **vendored into the repo**. The demo asks developers to paste a **live production
  bearer token** into a form, so it must not load executable code from third-party CDNs — a
  compromise at any CDN could read that token. The page makes **zero** off-origin requests.
- `assets/` — DxQSO's own images (logo).

### Running it locally

It is plain static HTML — serve the repo root with any static server:

```bash
python3 -m http.server 8000     # then open http://localhost:8000
```

### Editing

Edit `index.html` and push to `main`; Vercel redeploys. Keep libraries **vendored** — do not
reintroduce a CDN `<script src>`. To update a library, replace the file under `vendor/<host>/<path>`
so the relative `url()` references inside the CSS keep resolving.
