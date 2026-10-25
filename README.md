# 교류 유효전력 계산기

정현파 전압·전류와 위상차로 평균 유효전력 계산

- Plan ID: E084
- App: https://nanalab.kr/eng-ac-real-power/
- Repository: https://github.com/NaNaCompany/eng-ac-real-power
- Formula: `P = V_rms I_rms cosφ`
- Output: 유효전력 P

## Model

V_rms,I_rms≥0, −180°≤φ≤180°. 같은 주파수 정현파 모델이며 음수 전력도 허용한다. 비정현파의 전체 역률·피상전력·무효전력은 출력하지 않는다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `100`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
