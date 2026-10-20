<h1 align="center">🌐 spectrogy.com</h1>

<p align="center">
  <i>The public face of Spectrogy, an optical liquid-intelligence platform: spectroscopy + embedded hardware + AI for real-time analysis of liquids.</i>
</p>

<p align="center">
  <a href="https://spectrogy.com"><img alt="spectrogy.com" src="https://img.shields.io/badge/live-spectrogy.com-0A7CFF"></a>
  <a href="https://pool.spectrogy.com"><img alt="pool" src="https://img.shields.io/badge/live-pool.spectrogy.com-00B8D4"></a>
  <a href="https://spectra.spectrogy.com"><img alt="spectra" src="https://img.shields.io/badge/live-spectra.spectrogy.com-7C4DFF"></a>
  <img alt="Firebase Hosting" src="https://img.shields.io/badge/Firebase-Hosting-FFCA28?logo=firebase&logoColor=black">
  <img alt="CI" src="https://img.shields.io/badge/CI-GitHub%20Actions-2088FF?logo=githubactions&logoColor=white">
</p>

> Plain HTML. No framework, no build step, no `node_modules` the size of a small moon.
> The physics is complicated enough already.

---

## Three sites, one repo

| Folder | Domain | What it's about |
|---|---|---|
| `/` | [spectrogy.com](https://spectrogy.com) | the platform: optical sensing for agriculture, water, beverages, biotech and industrial processes |
| `pool/` | [pool.spectrogy.com](https://pool.spectrogy.com) | continuous biological monitoring for commercial pools: bacterial load, biofilm and organic contamination in real time, no reagents |
| `spectra/` | [spectra.spectrogy.com](https://spectra.spectrogy.com) | **Spectra**, a pocket breath instrument: 14 channels from a single exhale |

### The science behind the marketing

Spectrogy sensors read liquids with light instead of reagents:

- **Light scattering & speckle dynamics**: particles in Brownian motion make laser speckle flicker. The flicker rate gives particle size, from viruses (~100 nm) to bacteria (~1 µm).
- **Autofluorescence**: living cells glow faintly under 405 nm light.
- **Deep-UV absorption**: nucleic acids and proteins absorb at 260–280 nm.
- **Machine learning**: turns those three signals into a verdict, continuously.

---

## Layout

```
├── index.html            spectrogy.com
├── images/  favicon/     assets (webp, because bandwidth is not free)
├── pool/                 pool.spectrogy.com   (own favicon + OG cover)
├── spectra/              spectra.spectrogy.com
├── robots.txt  sitemap.xml
├── firebase.json         three hosting targets: main · pool · spectra
└── .github/workflows/    deploy on merge, preview channel on PR
```

## Deploy

Every push to `main` deploys to Firebase Hosting through GitHub Actions. A pull request gets its own preview URL.

```bash
# manual deploy, if you enjoy typing
firebase deploy --only hosting          # all three targets
firebase deploy --only hosting:pool     # just one
```

Preview locally with any static server, for example `python3 -m http.server 8000`.

---

## Related

- 🔒 `spectrogy-server`: FastAPI + ML backend *(private)*
- 🔒 `spectrogy-firmware`: STM32 + ESP8266 sensor firmware & KiCad hardware *(private)*
- 📊 [app.spectrogy.com](https://app.spectrogy.com): the fleet dashboard

---

<p align="center">
  Built by <a href="https://github.com/mrBurma"><b>Dmitriy Ageev</b></a>, physicist · inventor · deep-tech founder of <a href="https://spectrogy.com">Spectrogy</a><br>
  <a href="https://boosty.to/ague/donate">❤️ Support on Boosty</a>: lessons, 3D models and code from real projects
</p>
<p align="center"><sub>© Spectrogy · site content and imagery all rights reserved</sub></p>
