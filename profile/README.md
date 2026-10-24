# NEM Lens

Open tools for looking closely at what happens in Australia's National
Electricity Market (NEM) during price spikes and other stress events.

**[Event library →](https://nem-lens.github.io/library/)**

The library replays real market events interval by interval: regional prices,
demand, what each fuel type generated, interconnector flows, binding
constraints, generator outages and AEMO's market notices. Every figure comes
directly from data AEMO publishes. We add no modelled or estimated values.

## Repositories

| Repo | What it does |
|------|--------------|
| [library](https://github.com/nem-lens/library) | The public event library and replay page, served on GitHub Pages |
| [monitor](https://github.com/nem-lens/monitor) | Finds events in AEMO's dispatch data and builds them into library entries |
| [aemo](https://github.com/nem-lens/aemo) | Rust library for reading AEMO's MMS data and the shared event schema |
| [der](https://github.com/nem-lens/der) | Household batteries and rooftop solar in the NEM, by region and month, from Clean Energy Regulator and AEMO data, with charts and headline figures |

Modelling tools for exploring how events might have played out differently are
in development.

## How events are chosen

An event is a run of 5-minute dispatch intervals where a region's price stays
high. Each event is tagged by year, season, region and severity, and by
conditions such as prices at the market cap or floor, AEMO interventions and
market suspension. The library covers events from January 2020 onward.

## Licence and data

Code is © Archie C. Chapman and contributors, released under the
[BSD 3-Clause licence](https://opensource.org/license/bsd-3-clause).
Market data © AEMO, used under AEMO's
[copyright permissions](https://www.aemo.com.au/privacy-and-legal-notices/copyright-permissions).
The der tables and charts are based on Clean Energy Regulator material
licensed under
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
The licence covers our code, not AEMO's or the CER's data. NEM Lens is
independent and is not affiliated with or endorsed by AEMO or the CER.
