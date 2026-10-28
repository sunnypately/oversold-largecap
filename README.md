# Oversold Large-Cap Growth Monitor

Companies worth $10B or more, with revenue up at least 20% year over year, that trade at least 25% below their 52-week high — ranked by the gap between the live price and a blended fundamental fair value (earnings multiple, sales multiple, street target).

Live at: `https://sunnypately.github.io/oversold-largecap/`

## Files

```
oversold-largecap/
├── index.html               the page (tabs: All large caps · AI-linked · Other sectors · Method)
└── data/
    ├── fundamentals.json    names on the screen, with fundamentals and fair values
    └── not_on_screen.json   large caps checked that failed the screen, with the reason
```

## Deploy

1. Upload the `oversold-largecap` folder to the root of the `sunnypately.github.io` repo (GitHub web UI: **Add file → Upload files**, drag the folder in).
2. Commit. GitHub Pages publishes it within a minute or two.

## Updating the data

Prices update live in the browser (Finnhub, every 5 minutes while open). The ticker list, fundamentals and fair values are rebuilt each NYSE trading day on the Claude dashboard. To bring this copy up to date, replace the two files in `data/` with fresh exports and commit — `index.html` doesn't need to change.

The page must be served over http(s) (GitHub Pages, or `python3 -m http.server` locally); opening `index.html` straight from disk can't load the data files.

Research tooling, not investment advice.
