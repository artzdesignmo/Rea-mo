# Rea Mo

**Paste a URL, get the build sheet.** A tiny zero-dependency browser tool that reverse-engineers how a public GitHub repo or website is built — live tech-stack detection, structure mapping, framework fingerprints, and honest heuristic verdicts.

## Features

- **GitHub repo analysis** (100% client-side via `api.github.com`): overview (stars, forks, license, size), releases (latest version with direct download links + previous versions), language breakdown bars, detected frameworks (from `package.json` + filenames), file-structure stats, project signals (CI, tests, Docker, docs), and a verdict section with clearly-labeled heuristics.
- **Website analysis**: fetches public HTML through CORS proxies, then extracts title/meta/headings, resource counts, framework fingerprints (React, Next.js, Vue, WordPress, Shopify, Tailwind, …), and internal vs external link ratio.
- **Optional AI interpretation (BYOK)**: plug in your own OpenAI-compatible endpoint + API key (stored only in your browser's localStorage) for a plain-language verdict. The tool is fully useful without a key — this is an add-on, never a requirement.
- **Honest by design**: no fake results, no fake "AI thinking" spinners, heuristic observations are always labeled as heuristic.
- EN/中文 UI toggle (default English), light print-lab aesthetic, works offline-first except the analyzed targets themselves.

## Usage

Open `index.html` in any modern browser (or host it on GitHub Pages). Paste one of:

- a GitHub repo URL (`https://github.com/owner/repo`) or `owner/repo` shorthand
- a website URL or bare domain (`example.com`)

Hit **Analyze** and get the dossier. That's it — no build step, no backend, no account.

## Try it

- `morluto/rea` — a huge polyglot monorepo; watch the language bars and signals light up.
- `https://openx-mo.vercel.app` — a minimal static site; compare its fingerprint with a heavy framework site.

## Notes

- GitHub's unauthenticated API allows ~60 requests/hour per IP; analyzing very large repos may take a few seconds.
- Website fetching depends on public CORS proxies (`allorigins`, `corsproxy.io`); if both fail the tool says so honestly instead of inventing data.

## Support

If Rea Mo is useful to you, you can support its development with a coffee:

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-FFDD00?logo=buymeacoffee&logoColor=black)](https://buymeacoffee.com/whynotartmoney)
