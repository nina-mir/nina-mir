<!-- Icons: Lucide via Iconify (accent #8957e5) · banners: assets/*.png · renders on GitHub -->

<p align="center">
  <img src="assets/header.png" alt="Nina Mir — software engineer // web / data" width="100%" />
</p>

## <img align="top" width="24" src="https://api.iconify.design/lucide/calendar-days.svg?color=%238957e5" /> &nbsp;August 2026

<img src="assets/section-open-source.png" alt="Open-source contributions" width="100%" />

**`mdn/browser-compat-data`** &nbsp;[#30171](https://github.com/mdn/browser-compat-data/pull/30171) &nbsp;![merged](https://img.shields.io/badge/merged-8250df?style=flat-square)

Corrected Firefox compat data for `FontFaceSet.values() / .keys() / .entries()`. Tested 11 iteration behaviors across Firefox 153 and Chrome 151 to establish which three subfeatures are broken and which work correctly — a distinction the original report never made.

![compat-data](https://img.shields.io/badge/compat--data-informational?style=flat-square) ![cross-browser testing](https://img.shields.io/badge/cross--browser_testing-informational?style=flat-square) ![JSON Schema](https://img.shields.io/badge/JSON_Schema-000000?style=flat-square&logo=json&logoColor=white) ![MDN](https://img.shields.io/badge/MDN-000000?style=flat-square&logo=mdnwebdocs&logoColor=white)

<br>

**`python-visualization/folium`** &nbsp;[#2263](https://github.com/python-visualization/folium/pull/2263) &nbsp;![merged](https://img.shields.io/badge/merged-8250df?style=flat-square)

Root-caused and fixed [issue #1520](https://github.com/python-visualization/folium/issues/1520) (open since 2021): GeoJSON tooltips/popups came up empty on multi-geometry features because `feature` never reached the child layers Leaflet wraps in a `FeatureGroup`. Fix verified against all eight geometry types plus nested `GeometryCollection`s, with a Selenium regression test.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Leaflet](https://img.shields.io/badge/Leaflet%2FJS-199900?style=flat-square&logo=leaflet&logoColor=white) ![Jinja2](https://img.shields.io/badge/Jinja2-B41717?style=flat-square&logo=jinja&logoColor=white) ![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white) ![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=flat-square&logo=selenium&logoColor=white)

<br>

**`traceroot-ai/traceroot`** &nbsp;[#1968](https://github.com/traceroot-ai/traceroot/pull/1968) &nbsp;![in review](https://img.shields.io/badge/in_review-1a7f37?style=flat-square)

Rewrote the Vercel AI integration docs for AI SDK v7, fixing [issue #1966](https://github.com/traceroot-ai/traceroot/issues/1966), which I filed. The page documented `experimental_telemetry`, which on `ai` 7.x emits nothing — silently, with no error. Running the page's own example unmodified produced 1 span; changing only the telemetry line to `@ai-sdk/otel` produced 5, including the `chat` LLM span and the `execute_tool` span the page's own "What Gets Captured" table promises.

![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=flat-square&logo=opentelemetry&logoColor=white) ![Vercel AI SDK](https://img.shields.io/badge/Vercel_AI_SDK-000000?style=flat-square&logo=vercel&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![docs](https://img.shields.io/badge/docs-informational?style=flat-square)


<br>

**`jupyterlab/jupyterlab`** &nbsp;[#19257](https://github.com/jupyterlab/jupyterlab/pull/19257) &nbsp;![in review](https://img.shields.io/badge/in_review-1a7f37?style=flat-square) &nbsp;![milestone 4.6.x](https://img.shields.io/badge/milestone_4.6.x-informational?style=flat-square)

Fixed the low-contrast variable names in the Debugger Variables panel, open since 2023. A CodeMirror syntax token was styling UI chrome text at 2.43:1 — below even the 3:1 large-text floor of WCAG SC 1.4.3. Swapping it for an existing `--jp-` theme token brings it to 8.49:1, and tracing the background to a `.positioning-region` element inside the `jp-tree-item` shadow root explained why Dark High Contrast never helped.

![accessibility](https://img.shields.io/badge/accessibility-informational?style=flat-square) ![WCAG contrast](https://img.shields.io/badge/WCAG_contrast-informational?style=flat-square) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![CSS](https://img.shields.io/badge/CSS-1572B6?style=flat-square&logo=css3&logoColor=white)

<br>

**`jupyterlab/jupyterlab`** &nbsp;[#19303](https://github.com/jupyterlab/jupyterlab/pull/19303) &nbsp;![in review](https://img.shields.io/badge/in_review-1a7f37?style=flat-square)

Fixed Alt+W not closing the current tab when focus sat outside the main area — open since 2018 with zero comments. The `application:close` keybinding was scoped to `.jp-Activity`, so it never fired unless focus was in a main-area widget, while File ▸ Close Tab worked from anywhere. A one-line selector change, plus a repro widened past the original report and five scenarios verified against `main` to show the modal and terminal behaviors are pre-existing.

![keybindings](https://img.shields.io/badge/keybindings-informational?style=flat-square) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![JSON Schema](https://img.shields.io/badge/JSON_Schema-000000?style=flat-square&logo=json&logoColor=white)

<br>

**`python-visualization/folium`** &nbsp;[#2274](https://github.com/python-visualization/folium/pull/2274) &nbsp;![in review](https://img.shields.io/badge/in_review-1a7f37?style=flat-square)

Upgraded Leaflet 1.9.3 → 1.9.4 at a maintainer's request, repairing a notebook test red on `main`. Leaflet 1.9.3 calls `layer.getElement()` unguarded and throws on any nested `FeatureGroup`; because the failing test skipped `verify_js_logs()`, the uncaught error lingered in the session-scoped driver's console log and surfaced in whichever later test read it first — not the page CI blamed. Reproduced by running the two tests in order; 76 passed, 1 xfailed locally.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Leaflet](https://img.shields.io/badge/Leaflet%2FJS-199900?style=flat-square&logo=leaflet&logoColor=white) ![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white) ![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=flat-square&logo=selenium&logoColor=white)


<details>
<summary><b>Also this month</b></summary>
<br>

- Filed [`adobe/react-spectrum` #10411](https://github.com/adobe/react-spectrum/issues/10411) with a live reproduction — the S2 docs playground was emitting Tooltip code samples that didn't typecheck; a maintainer shipped the fix the next day.
- Posted browser-tested findings on [`react-spectrum` #8027](https://github.com/adobe/react-spectrum/issues/8027) and [`mdn/content` #45005](https://github.com/mdn/content/pull/45005), including the negative results.

</details>

---

## <img align="top" width="24" src="https://api.iconify.design/lucide/calendar-days.svg?color=%238957e5" /> &nbsp;July 2026

### <img align="top" width="20" src="https://api.iconify.design/lucide/puzzle.svg?color=%238957e5" /> &nbsp;Save Image 'n Context — Manifest V3 Chrome extension

A research tool: right-click any web image to download it **and** log a local citation record of its source — page URL/title, canonical URL, Open Graph metadata, alt text, figure caption, plus the nearest heading/paragraph/link via deterministic DOM heuristics.

- **Privacy-first architecture** — a service worker paired with an on-demand content script using `activeTab` + `scripting` permissions; zero background access to browsing data.
- **Handles real-world messiness** — lazy-loaded image attributes, duplicate-capture detection, retry logic, graceful fallbacks on restricted pages.
- **Local & exportable** — up to 5,000 records live entirely in `chrome.storage.local`, reviewable on an options page and exportable as JSON/CSV (CSV hardened against spreadsheet formula injection).

![Chrome Extension](https://img.shields.io/badge/Chrome_Extension-4285F4?style=flat-square&logo=googlechrome&logoColor=white) ![Manifest V3](https://img.shields.io/badge/Manifest_V3-4285F4?style=flat-square) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

[![Get it on the Chrome Web Store](https://img.shields.io/badge/Get_it_on_the_Chrome_Web_Store-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white)](https://chromewebstore.google.com/detail/save-image-n-context/ikfnmdlkdmmjfoinfgmkccloejgmhmil) &nbsp; [![Source](https://img.shields.io/badge/Source-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/nina-mir/save-image-n-context)

---

<details>
<summary><h2><img align="top" width="22" src="https://api.iconify.design/lucide/calendar-days.svg?color=%238957e5" /> &nbsp;June 2026 — Snarp Profanity Index</h2></summary>
<br>

### <img align="top" width="20" src="https://api.iconify.design/lucide/chart-column.svg?color=%238957e5" /> &nbsp;Snarp Profanity Index — interactive dashboard

Visualizes how often different categories of profanity appear across 52 college-sports YouTube videos by a popular creator — to find out which collegiate rivalries are the most controversial *linguistically*.

- **The workflow** — scrape audio via the YouTube API ➜ transcribe with the Whisper neural network on Hugging Face ➜ analyze transcripts to categorize terms.
- **Interactive** — charts built with SVG & D3.js, plus full-text search across all transcripts.

![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white) ![YouTube API](https://img.shields.io/badge/YouTube_API-FF0000?style=flat-square&logo=youtube&logoColor=white) ![Whisper](https://img.shields.io/badge/Whisper-412991?style=flat-square&logo=openai&logoColor=white) ![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black) ![D3.js](https://img.shields.io/badge/D3.js-F9A03C?style=flat-square&logo=d3dotjs&logoColor=white)

[![Live demo](https://img.shields.io/badge/Live_demo-2ea44f?style=for-the-badge)](https://nina-mir.github.io/snarp-analysis/) &nbsp; [![Source](https://img.shields.io/badge/Source-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/nina-mir/snarp-analysis)

</details>

<details>
<summary><h2><img align="top" width="22" src="https://api.iconify.design/lucide/calendar-days.svg?color=%238957e5" /> &nbsp;Spring 2026 — Kopani</h2></summary>
<br>

### <img align="top" width="20" src="https://api.iconify.design/lucide/library-big.svg?color=%238957e5" /> &nbsp;Kopani — discovery infrastructure for independent literature

An MVP platform that indexes literary and art pieces published by independent journals *without republishing copyrighted material*.

- **Data pipeline** — scraping, ingestion & metadata-modeling workflows normalize journal content into structured, searchable records: titles, journals, authors, translators, visual artists, genres, keywords & reading time (Gemini AI / Colab notebook).
- **Discovery experience** — helps readers browse real pieces, return to the original journal sources, and (future) explore a contributor graph linking writers, artists, institutions, journals & publications.

![Astro](https://img.shields.io/badge/Astro-BC52EE?style=flat-square&logo=astro&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white) ![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white)

> [!TIP]
> Presented at the Perplexity AI *Billion Dollar Pitch* competition.

[![Live demo](https://img.shields.io/badge/Live_demo-2ea44f?style=for-the-badge)](https://kopani.netlify.app/)

</details>

<details>
<summary><h2><img align="top" width="22" src="https://api.iconify.design/lucide/calendar-days.svg?color=%238957e5" /> &nbsp;October 2025 — SF Film Locations RAG</h2></summary>
<br>

### <img align="top" width="20" src="https://api.iconify.design/lucide/clapperboard.svg?color=%238957e5" /> &nbsp;NLP-to-GeoPandas RAG pipeline

A full-stack RAG pipeline to chat with the [Film Locations in San Francisco dataset](https://data.sfgov.org/Culture-and-Recreation/Film-Locations-in-San-Francisco/yitu-d5am/about_data). Completed during a DigitalOcean / Auth0 hackathon in San Francisco on Oct 18, 2025.

![Gemini](https://img.shields.io/badge/Gemini_Flash-8E75B2?style=flat-square&logo=googlegemini&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white) ![GeoPandas](https://img.shields.io/badge/GeoPandas-139C5A?style=flat-square) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white) ![Folium](https://img.shields.io/badge/Folium_%28Leaflet%29-199900?style=flat-square&logo=leaflet&logoColor=white)

[![Live demo](https://img.shields.io/badge/Live_demo-2ea44f?style=for-the-badge)](https://film-hackathon-app-68quvgslnrkvpxtxasnq7c.streamlit.app/) &nbsp; [![Source](https://img.shields.io/badge/Source-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/nina-mir/DigitalOcean-hackathon-FILM-2025)

</details>

<details>
<summary><h2><img align="top" width="22" src="https://api.iconify.design/lucide/calendar-days.svg?color=%238957e5" /> &nbsp;2025 — WindBorne constellation data pipeline</h2></summary>
<br>

### <img align="top" width="20" src="https://api.iconify.design/lucide/radio-tower.svg?color=%238957e5" /> &nbsp;Live constellation visualizations

A full-stack project ingesting data from WindBorne Systems' live constellation API, feeding two D3.js plots:

- A **world map** displaying each flight trajectory over a 24-hour interval.
- A **Sankey chart** showing the start/end region of each trajectory (via geonames.org and nominatim.openstreetmap.org APIs).

The project runs an automated pipeline that fetches and processes new data hourly on an Ubuntu cloud server, and uses Cloudflare Workers to edge-cache the data files.

![D3.js](https://img.shields.io/badge/D3.js-F9A03C?style=flat-square&logo=d3dotjs&logoColor=white) ![Cloudflare Workers](https://img.shields.io/badge/Cloudflare_Workers-F38020?style=flat-square&logo=cloudflare&logoColor=white) ![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white)

[![Live demo](https://img.shields.io/badge/Live_demo-2ea44f?style=for-the-badge)](https://nina-mir.github.io/windborne-job-application/)

</details>

<details>
<summary><h2><img align="top" width="22" src="https://api.iconify.design/lucide/calendar-days.svg?color=%238957e5" /> &nbsp;Summer 2025 — Taschen-Dolmetcher.Revisited</h2></summary>
<br>

### <img align="top" width="20" src="https://api.iconify.design/lucide/gamepad-2.svg?color=%238957e5" /> &nbsp;Multilingual language-learning web game

A web game for people learning Russian / English / German. Inspired by real events on the Eastern Front from 1941–1945, it educates users about Holocaust history through historical materials and witnesses' artworks.

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) ![Storybook](https://img.shields.io/badge/Storybook-FF4785?style=flat-square&logo=storybook&logoColor=white)

[![Play it](https://img.shields.io/badge/Play_it-2ea44f?style=for-the-badge)](https://nina-mir.github.io/taschen-dolmetcher/)

> [!NOTE]
> Suggestions welcome — [open an issue](https://github.com/nina-mir/taschen-dolmetcher) or email **[nina@sfsu.edu](mailto:nina@sfsu.edu)**.

</details>

<details>
<summary><h2><img align="top" width="22" src="https://api.iconify.design/lucide/calendar-days.svg?color=%238957e5" /> &nbsp;Spring 2025 — The Hell of Treblinka</h2></summary>
<br>

### <img align="top" width="20" src="https://api.iconify.design/lucide/book-open-text.svg?color=%238957e5" /> &nbsp;Modern responsive typesetting

Typeset an important essay by Vasily Grossman — *"The Hell of Treblinka"* — so readers could have a modern, responsive reading experience.

[![Read it](https://img.shields.io/badge/Read_it-2ea44f?style=for-the-badge)](https://nina-mir.github.io/the-treblinka-hell/)

</details>
