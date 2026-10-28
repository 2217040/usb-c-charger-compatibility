# USB-C charger × device compatibility and charging time

For every pair of popular devices (phones, tablets, laptops, handheld consoles) and chargers: will it charge, the power the two negotiate, whether that is fast charging, and estimated 0–50% and 0–100% charging times. Device and charger specs come from the makers’ official pages.

Maintained by **[Can It Charge? (canitcharge.com)](https://canitcharge.com/)**. The files here are the same numbers the site shows, refreshed from the site every week by a GitHub Action.

### `data/charger-compatibility.csv` — Charger compatibility (940 rows)

Live version: <https://canitcharge.com/data/charger-compatibility.csv> · shown on <https://canitcharge.com/devices/>

| Column | Meaning |
|---|---|
| `device / device_brand / category` | Device and its type (phone, tablet, laptop, handheld) |
| `charger / charger_brand / charger_max_w` | Charger and its maximum output |
| `negotiated_w` | Power the pair settles on (USB-C PD / PPS / vendor protocols) |
| `verdict` | full speed, standard, slow, too weak or won’t charge |
| `limited_by` | What caps the power: the charger or the device |
| `minutes_0_to_50 / minutes_0_to_100` | Estimated charging time |
| `time_basis` | manufacturer (scaled from a published charging time) or battery (from capacity); empty when no time can be estimated |
| `page` | Page on canitcharge.com with the full answer and sources |

## How the numbers are made

Negotiated power = the lower of what the charger can deliver over the shared protocol and what the device accepts. Times scale the maker’s published charging time where there is one, otherwise battery energy ÷ power at 85% efficiency with a taper for the last 50%. Specs only from manufacturers’ official pages. Full method: <https://canitcharge.com/how-we-calculate/>.

## License and attribution

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — free to use, share and adapt, including commercially, with attribution:

> Source: Can It Charge? (canitcharge.com) — https://canitcharge.com/devices/

Spotted a wrong value? Open an issue with a link to the official source.
