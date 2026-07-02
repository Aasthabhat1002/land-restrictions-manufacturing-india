# Do Land Ownership Restrictions Suppress Manufacturing Investment in India?

MSc dissertation, University of Warwick, supervised by Professor Nathan Canen. Work in progress, June 2026.

## Question

India has restricted outside land ownership across roughly a third of its states since colonial and early independence era policy. Property rights theory says this should suppress investment, since a firm that cannot acquire land cannot build a plant or collateralise the asset. But communities with strong internal capital networks could partly substitute for excluded outside investors. Which effect dominates for manufacturing investment specifically had not been tested directly.

## Approach

A triple-difference design on 298,180 firm-year observations from India's Annual Survey of Industries, 18 states, 2003 to 2023. Rather than comparing restricted states to unrestricted ones directly, the design compares land-intensive firms (cement, steel, food processing) to land-light firms (electronics, pharma) within the same state and year. State by year fixed effects absorb everything else that changed at the same time, including COVID-19. This isolates the investment gap that's specifically attributable to the land restriction, not to whatever else differs between restricted and unrestricted states.

Three legal changes sharpen the identification further:
- August 2019: Article 35A abrogated in Jammu & Kashmir, the only removal of a constitutionally embedded land restriction in Indian history
- December 2019: Manipur moves the opposite direction, Inner Line Permit extended to the whole state
- 2018 to 2022: Uttarakhand relaxes then reinstates its statutory restriction

The J&K case is evaluated separately with synthetic control against always-restricted donor states.

## Result

Land-intensive firms in restricted states invest about 23% less in fixed capital than land-light firms in the same state and year (β = −0.228, p = 0.009). Employment is unaffected, which points to the restriction working through capital accumulation rather than labour demand. Constitutionally embedded restrictions produce roughly twice the investment gap of statutory ones, consistent with investors pricing in how hard a restriction is to reverse. Following the J&K abrogation, aggregate manufacturing investment rose to about 24 log points above the synthetic counterfactual within four years. Results hold under double machine learning with LASSO.

## Repository contents

- `paper/` — full dissertation writeup
- `code/` — data cleaning, the triple-difference regressions, the J&K synthetic control, and the double ML robustness check
- `data/` — not included; the Annual Survey of Industries microdata is restricted-access and not mine to redistribute. Cleaning scripts assume a raw ASI extract as input.

## Methods used

Triple-difference (DDD), state by year fixed effects, synthetic control, double machine learning (LASSO), wild cluster bootstrap inference.
