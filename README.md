# Dharma Japa Lite (free version)

English free version of Dharma Japa. It is derived from the Premium version (repo `dharma-japa`) and mirrors the Spanish free version (`japa-movil-free`), with these locks:

**Open:** deities Ganesha and Shiva · malas Rudraksha and Sphatik (crystal) · Taanpura audio base · all mantras (except the planets) · video backgrounds of Durga (Simhavahini I) and Hanuman (Veera) · store · share app · install guide (button "? TUTORIAL & INSTALLATION", PDF `pdf/Installation-Guide-Dharma-Japa-Lite.pdf`) · tutorial "Introduction to Mantras".

**Locked (notice to get Premium):** other deities, the 9 planets, other malas, Deep Peace and Cosmos bases, planet mantras and other backgrounds. For backgrounds, the notice includes a mini player with a short preview (`video/preview/`).

Purchase link: https://payhip.com/b/JiEve

**Rituals:** the Rituals menu is hidden in the English version (as in Premium) until the ritual pages are translated. When they are, remove the `#jp-rituales-container { display: none !important; }` line in `index.html`, copy `rituales/` from the Premium repo and set `FREE.ritualPreview` (e.g. `{ ganesha: 3 }`).

## Changing what is open
In `index.html`, find the `var FREE = {` block and edit the `deidades`, `malas` and `fondos` lists. If you open something new, also copy its files from the Premium repo (e.g. the full video `video/fondo-xxx.mp4` or the 28 images of the mala).

## Offline
`sw.js` is a service worker: once opened with a connection, the app opens even without network (or if the network is blocked). Bump `VERSION` in `sw.js` to force every phone to download everything again.

## Share link
`SHARE_URL` in `index.html` is the link sent by the Share button.
