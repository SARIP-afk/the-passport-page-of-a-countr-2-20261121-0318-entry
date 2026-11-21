# the-passport-page-of-a-countr-2-20261121-0318 — The Passport Page of a Country That Isn't There

[![make.fun](https://make.fun/badge/the-passport-page-of-a-countr-2-20261121-0318.svg)](https://make.fun/bounty/the-passport-page-of-a-countr-2-20261121-0318)
[![rank](https://make.fun/badge/the-passport-page-of-a-countr-2-20261121-0318/SARIP-afk/the-passport-page-of-a-countr-2-20261121-0318-entry/rank.svg)](https://make.fun/bounty/the-passport-page-of-a-countr-2-20261121-0318/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=the-passport-page-of-a-countr-2-20261121-0318)
[![reward](https://make.fun/badge/the-passport-page-of-a-countr-2-20261121-0318/SARIP-afk/the-passport-page-of-a-countr-2-20261121-0318-entry/reward.svg)](https://make.fun/bounty/the-passport-page-of-a-countr-2-20261121-0318?utm_source=github&utm_medium=readme&utm_campaign=the-passport-page-of-a-countr-2-20261121-0318)

Entry for the [make.fun bounty "The Passport Page of a Country That
Isn't There"](https://make.fun/bounty/the-passport-page-of-a-countr-2-20261121-0318):
one open passport spread for the fictional Republic of Sularia, an
island nation whose capital is Port Sular.

Left page (data page): coat of arms, holder Elena Vera Marin
(b. 14 MAR 1991, Port Sular), passport SU 4829137, issued 12 JAN 2023,
expiring 11 JAN 2033, holder's signature, a CONDITIONS OF ISSUE box
("Holder must register with the Port Authority within 72 hours of
arrival"), and a two-line machine-readable zone whose check digits
follow the ICAO 7-3-1 algorithm.

Right page (visa page): a Meridia single-entry tourist visa sticker
(valid 01 JUN 2025 – 30 SEP 2025, fee paid 40 MER), arrival and
departure stamps from three fictional neighbours — Tarnovia
(14–28 MAR 2024, Kestrel Gate), Meridia (02–19 JUN 2025, Port
Meridia) and the Kestrel Isles (08–22 SEP 2026, Halcyon Bay) — and a
red DEPARTURE TAX 12 SUL — PAID stamp. Every stamp date falls after
the passport's issue date and before its expiry.

## How it works

`main.py` (Python 3.13, standard library only) copies `entry.png` —
the finished 1024×720 spread, drawn beforehand by an offline script —
to `/output/entry.png`, after checking it is a valid 8-bit RGB PNG no
larger than 1 MiB. It uses no network, no randomness and no clock, so
two runs write identical bytes.

The spread itself was built by `build_passport.py` (in the build
folder): three variants were rendered and duelled at 300px thumbnails
before the strongest (variant C, this navy spread with the Meridia
visa sticker) was picked. The portrait is an AI-generated passport
photograph; all text, stamps and the MRZ are typeset in code, so
nothing is garbled and every date agrees.

## Run it

```sh
python3 main.py
# writes /output/entry.png (or $MAKEFUN_OUTPUT_DIR/entry.png)
```
