## [August 2026]
 
#### Started contributing upstream to open source — three PRs so far, in three different ecosystems
 
**[mdn/browser-compat-data #30171](https://github.com/mdn/browser-compat-data/pull/30171) — ✅ merged**
Corrected Firefox compat data for `FontFaceSet.values()/.keys()/.entries()`: tested 11 iteration behaviors across Firefox 153 and Chrome 151 to establish which three subfeatures are broken and which work correctly — a distinction the original report didn't make.
`compat-data` `cross-browser testing` `JSON schema` `MDN`
 
**[python-visualization/folium #2263](https://github.com/python-visualization/folium/pull/2263) — 🔄 in review**
Root-caused and fixed [issue #1520](https://github.com/python-visualization/folium/issues/1520) (open since 2021): GeoJSON tooltips/popups came up empty on multi-geometry features because `feature` never reached the child layers Leaflet wraps in a `FeatureGroup` — fix verified against all eight geometry types plus nested `GeometryCollection`s, with a Selenium regression test.
`Python` `Leaflet/JS` `Jinja2` `pytest` `Selenium`
 
**[jupyterlab/jupyterlab #19257](https://github.com/jupyterlab/jupyterlab/pull/19257) — 🔄 open**
Fixes the low-contrast variable names in the Debugger Variables panel by swapping a hard-coded color for an existing `--jp-` theme token, so the text stays readable in both light and dark themes.
`accessibility` `WCAG contrast` `TypeScript` `CSS`
 
#### also this month
 
- filed [adobe/react-spectrum #10411](https://github.com/adobe/react-spectrum/issues/10411) with a live reproduction — the S2 docs playground was emitting Tooltip code samples that didn't typecheck; a maintainer shipped the fix the next day
- posted browser-tested findings on [react-spectrum #8027](https://github.com/adobe/react-spectrum/issues/8027) and [mdn/content #45005](https://github.com/mdn/content/pull/45005), including the negative results
<hr>
## [July 2026]

#### Built & published **Save Image 'n Context** — a Manifest V3 Chrome extension for researchers: right-click any web image to download it *and* log a local citation record of its source (page URL/title, canonical URL, Open Graph metadata, alt text, figure caption, plus the nearest heading/paragraph/link via deterministic DOM heuristics)

- privacy-first architecture: a service worker paired with an on-demand content script using `activeTab` + `scripting` permissions — zero background access to browsing data
- handles real-world messiness: lazy-loaded image attributes, duplicate-capture detection, retry logic, graceful fallbacks on restricted pages
- up to 5,000 records live entirely in `chrome.storage.local`, reviewable on an options page & exportable as JSON/CSV (CSV hardened against spreadsheet formula injection)

#### get it on the Chrome Web Store ➡️ https://chromewebstore.google.com/detail/save-image-n-context/ikfnmdlkdmmjfoinfgmkccloejgmhmil

#### source code ➡️ https://github.com/nina-mir/save-image-n-context

<hr>

## [June 2026]

#### Built the **Snarp Profanity Index** — an interactive dashboard visualizing the frequency of various categories of profanities across 52 college-sports YouTube videos by a popular creator, to find out which collegiate rivalries are the most controversial *linguistically* 😄

- the workflow: scraping audio via the YouTube API ➜ transcribing with the Whisper neural network on HuggingFace ➜ analyzing the transcripts to categorize terms
- interactive charts made with svg & d3.js + full-text search across all transcripts
- tech stack: Google Colab, YouTube API, Whisper, Claude AI, GitHub Pages

#### check it out ➡️ https://nina-mir.github.io/snarp-analysis/

#### source code ➡️ https://github.com/nina-mir/snarp-analysis

<hr>

## [Spring 2026]

#### Built **Kopani** — MVP discovery infrastructure for independent literature: a platform that indexes literary/art pieces published by independent journals *without republishing copyrighted material*

- data scraping, ingestion & metadata-modeling workflows normalize journal content into structured, searchable records: titles, journals, authors, translators, visual artists, genres, keywords & reading time (Gemini AI / Colab notebook)
- the discovery experience helps readers browse real pieces, return to the original journal sources, and (in the future) explore a contributor graph linking writers, artists, institutions, journals & publications
- tech stack: Astro + TailwindCSS frontend, SQLite backend deployed on Netlify, browser localStorage for user data retention

#### presented at the Perplexity AI Billion Dollar Pitch competition

#### check it out ➡️ https://kopani.netlify.app/

<hr>

## [October 2025]

#### Built a full-stack RAG pipeline (NLP-2-GeoPandas Dataframe) to chat with [Film Locations in San Francisco dataset](https://data.sfgov.org/Culture-and-Recreation/Film-Locations-in-San-Francisco/yitu-d5am/about_data)

- tech stack: Google Gemini AI model Flash, Python, Streamlit Cloud, GeoPandas, SQLite, Folium (Leaflet) map
- The full design, specs and code are available <https://github.com/nina-mir/DigitalOcean-hackathon-FILM-2025>

#### This app was completed during a DigitalOcean/Auth0 sponsored hackathon event on Oct-18-2025 in San Francisco, CA

#### check it out https://film-hackathon-app-68quvgslnrkvpxtxasnq7c.streamlit.app/

<hr>

#### Built a full stack project ingesting data from WindBorne Systems' live constellation API to be used in two plots made by d3.js

- a worldmap displaying each flight trajectory in a 24-hr interval
- a Sankey chart to display the starting/ending region of each trajectory using geonames.org and nominatim.openstreetmap.org APIs

#### The project depends on an automated datapipeline that fetches and processes new data hourly [on an Ubuntu cloud server] and uses Cloudflare Workers to edge-cache the data files  

#### check it out <https://nina-mir.github.io/windborne-job-application/>  

## [summer 2025]

#### Released **Taschen-Doelmetcher.Revisited** — a multilingual web-game for language learning & practice for folks who are learning Russian/English/German (React, TypeScript, TailwindCSS, Storybook). This game is heavily inspired by real events that happened from 1941-1945 in the Eastern Front in Europe, and educates users about Holocaust history through historical materials and witnesses' artworks

#### check the game out <https://nina-mir.github.io/taschen-dolmetcher/>
  
> #### if you have any suggestions please open an issue here: <https://github.com/nina-mir/taschen-dolmetcher> or email me directly at **<nina@sfsu.edu>**

## [spring 2025]

#### recently typeset an important essay by Vasily Grossman, so folks could have a modern, responsive reading experience of the "The Hell of Treblinka."

Read it: https://nina-mir.github.io/the-treblinka-hell/
