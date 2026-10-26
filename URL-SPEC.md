# Scrollcore mockup URL pattern
BASE = https://cdn.jsdelivr.net/gh/scrollcore/scrollcore-mockups@v2
URL  = {BASE}/{line}/{model-slug}/{colour}.webp
line: aero | ridge | trail | lumen
model-slug: lowercase, spaces->hyphens (iPhone 17 Pro Max -> iphone-17-pro-max)
colour: slug as in manifest (e.g. blush-pink, rose-gold)
Images: 1000x1000 WebP q80, ~22 KB each. manifest.json lists every valid {line, model, colour, path}.
Lumen covers iPhone 14-17 only; tough lines cover 13 mini - 17 Pro Max incl. 17 Air.
Site behaviour: on model or colour change, set <img src> to URL; if combo missing in manifest, fall back to the line's default photo. Lumen: show note "Shown on a grey phone; case is clear."
