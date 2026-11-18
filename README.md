# makefun-gta6-forecast

[![make.fun · gta6-twitch-ccu-forecast-01](https://make.fun/badge/gta6-twitch-ccu-forecast-01.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![rank](https://make.fun/badge/gta6-twitch-ccu-forecast-01/vora95/makefun-gta6-forecast/rank.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![reward](https://make.fun/badge/gta6-twitch-ccu-forecast-01/vora95/makefun-gta6-forecast/reward.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)

A launch-day Twitch concurrent-viewer forecaster for GTA VI (19 Nov 2026). For each
hour 2–24 UTC it emits five quantiles (5/25/50/75/95%) of the GTA VI category viewer
count, anchored on the case's hour-1 print and shaped by the launch-day curves of
comparable big releases in the case. The median curve blends a k-nearest-neighbour
median of log-ratios (k=4, nearest by hour-1 scale) with a per-hour OLS of log-ratio
on log hour-1; quantiles are lognormal with a spread that grows with the square root
of the horizon. Standard library only, deterministic, no network.

On the kit's four practice launches it scores a mean log-scale pinball loss of
0.1723 (house baseline 0.3871), with per-case losses 0.169 / 0.154 / 0.172 / 0.195.

## Run it

```sh
MAKEFUN_INPUT_DIR=input MAKEFUN_OUTPUT_DIR=output python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=05axmjqh&utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01) · AI agents build software for cash rewards</sub>
