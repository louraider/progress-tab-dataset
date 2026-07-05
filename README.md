# World Progress Dataset

A small, **sourced and checkable** dataset of long-run world-progress indicators — child
mortality, extreme poverty, disease eradication, clean energy, schooling, and more. Every
figure is attributed to its primary source (Our World in Data, the WHO, the World Bank, UNICEF, the UN, IRENA, The Carter Center, the ILO, and FAO).

This is the open dataset behind **[Progress Tab](https://progresstab.app)** — a free Chrome extension that
shows one verified statistic about global progress on each new tab. You guess the number
first, then see the real one: the guess-then-reveal calibration method from Hans Rosling's
*Factfulness*, turned into a daily habit.

> **Accuracy, not optimism.** Each indicator is dual-frame — it holds both sides at once:
> measurably better than it was, *and* still unfinished. This is not a "good news" feed.

## Indicators (24)

| Indicator | Latest | Change | As of | Source |
|---|---|---|---|---|
| Access to clean cooking | 74.4% | +25 pts since 2000 | 2023 | [World Bank (WHO Household Energy DB)](https://data.worldbank.org/indicator/EG.CFT.ACCS.ZS?locations=1W) |
| Access to electricity | 91% | +13 pts since 2000 | 2022 | [Our World in Data](https://ourworldindata.org/energy-access) |
| Adult literacy | 87% | +12 pts since 1990 | 2020 | [Our World in Data](https://ourworldindata.org/literacy) |
| Basic sanitation access | 82.2% | +27 pts since 2000 | 2024 | [World Bank (WHO/UNICEF JMP)](https://data.worldbank.org/indicator/SH.STA.BASS.ZS?locations=1W) |
| Child mortality (under 5) | 37 per 1,000 | −60% since 1990 | 2022 | [Our World in Data](https://ourworldindata.org/child-mortality) |
| Children in child labour | 7.8% | −8.2 pts since 2000 | 2024 | [ILO & UNICEF (Global Estimates 2024)](https://data.unicef.org/resources/child-labour-global-estimates-2024/) |
| Chronic hunger worldwide | 8.2% | −4.5 pts since 2000 | 2024 | [Our World in Data (FAO, SOFI 2025)](https://ourworldindata.org/grapher/prevalence-of-undernourishment) |
| Cost of solar electricity | 0.044 $/kWh | −90% since 2010 | 2023 | [IRENA, Renewable Power Generation Costs in 2023](https://www.irena.org/Publications/2024/Sep/Renewable-Power-Generation-Costs-in-2023) |
| Deaths from natural disasters | around 10× lower than a century ago | −90%+ since the 1920s | 2020 | [Our World in Data](https://ourworldindata.org/natural-disasters) |
| Deaths from smallpox | 0 (eradicated 1980) | ≈2M/year in the 1960s → 0 | 1980 | [Our World in Data](https://ourworldindata.org/smallpox) |
| DTP3 vaccine coverage | 84% | from 20% (1980) to 84% | 2023 | [Our World in Data (WHO/UNICEF WUENIC)](https://ourworldindata.org/grapher/share-of-children-immunized-dtp3) |
| Extreme poverty worldwide | 8.5% | −78% since 1990 | 2019 | [Our World in Data](https://ourworldindata.org/poverty) |
| Guinea worm disease | 14 cases (2023) | from ≈3.5M in 1986 | 2023 | [The Carter Center](https://www.cartercenter.org/health/guinea_worm/case-totals.html) |
| HIV/AIDS death rate | 9.9 per 100,000 | −63% from 2000s peak | 2023 | [Our World in Data (IHME, GBD 2023)](https://ourworldindata.org/grapher/hiv-death-rates) |
| Internet access | 67% | from <1% in 1995 | 2023 | [Our World in Data](https://ourworldindata.org/internet) |
| Life expectancy | 73 years | +41 years since 1900 | 2023 | [Our World in Data](https://ourworldindata.org/life-expectancy) |
| Malaria death rate | 9.6 per 100,000 | −34% since 2000 | 2023 | [Our World in Data (IHME, GBD 2023)](https://ourworldindata.org/grapher/malaria-death-rates) |
| Maternal mortality | 223 per 100,000 | −35% since 2000 | 2020 | [Our World in Data](https://ourworldindata.org/maternal-mortality) |
| Ozone-depleting substances | −99% | layer recovery by ~2066 | 2024 | [Our World in Data](https://ourworldindata.org/ozone-layer) |
| Polio (wild virus) | ≈12 cases (2023) | −99.9% since 1988 | 2023 | [Our World in Data](https://ourworldindata.org/polio) |
| Safe drinking water at home | 74% | +2.2B people since 2000 | 2024 | [Our World in Data](https://ourworldindata.org/clean-water-sanitation) |
| Share of electricity from solar and wind | 13.4% | from 0.2% in 2000 | 2023 | [Our World in Data](https://ourworldindata.org/renewable-energy) |
| Tuberculosis death rate | 14.7 per 100,000 | −69% since 2000 | 2024 | [Our World in Data (WHO)](https://ourworldindata.org/grapher/tuberculosis-death-rate) |
| Years of schooling (adults) | 8.8 years | +2.9 years since 1990 | 2023 | [Our World in Data (UNDP, HDR 2025)](https://ourworldindata.org/grapher/average-years-of-schooling) |

## Files

- [`facts.json`](facts.json) — the full dataset: value, unit, time series (`chart`), change,
  direction, a one-line "why", and per-figure source + license + access date.
- [`facts.csv`](facts.csv) — the same records, flat, one row per indicator.

## How each figure is framed

Each record carries the **current value**, the **trend**, the **direction that counts as
progress** (`direction_better`), a short **why** attributing the change to systems (vaccines,
sanitation, cheaper solar) rather than individuals, and a link to the **primary source** and
the specific Progress Tab page for that indicator.

## Sources & provenance

Figures come from Our World in Data, the WHO, the World Bank, UNICEF, the UN, IRENA, The Carter Center, the ILO, and FAO. The specific source, its URL, its license, and the date
it was accessed are recorded **per figure** in the `source` object (`facts.json`) and the
`source_*` columns (`facts.csv`). Prefer citing the underlying source named on each record.

## License

The **compilation** (this dataset's selection, structure, labels, and framing) is released
under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — reuse freely with
attribution to *Progress Tab (https://progresstab.app)*.

Each **underlying figure** remains under its own source's terms (most are CC BY 4.0 via Our
World in Data; consult the `source.license` field and the source link for the exact terms of
each one). Attribute the original source when you reuse a specific number.

## Use it

- **Browse the facts, guess-first:** https://progresstab.app
- **Add the extension (Chrome / Edge / Brave):** https://chromewebstore.google.com/detail/progress-tab/oelmgnolihiejfdnohfkoknhgdohnfme
- **Reuse the data:** clone this repo, or read `facts.json` / `facts.csv` directly.

---

*Generated from the Progress Tab fact set. Corrections and better sources welcome — open an issue.*
