# bg-board-mirror

A scheduled mirror of the Hearthstone Battlegrounds official leaderboards, refreshed
every ~30 minutes from [BGrank's public mirror](https://github.com/IBM5100o/BGrank_bot)
(`bgrank.fly.dev`) by a GitHub Action.

It exists because `fly.dev` is unreliable or unreachable from some networks
(notably many Russian ISPs), while `raw.githubusercontent.com` stays accessible.
[MMRadar](https://github.com/lowerman/MMRadar_HDT_BG) falls back to this mirror
automatically when the primary source cannot be reached.

## Data

Branch `mirror`, verbatim BGrank format (`playerName rating` lines separated by `\n<br />`):

```
https://raw.githubusercontent.com/lowerman/bg-board-mirror/mirror/EU.txt
https://raw.githubusercontent.com/lowerman/bg-board-mirror/mirror/US.txt
https://raw.githubusercontent.com/lowerman/bg-board-mirror/mirror/AP.txt
https://raw.githubusercontent.com/lowerman/bg-board-mirror/mirror/CN.txt
```

plus `*_duo.txt` variants and `updated.txt` — a manifest of per-board UTC refresh times.

Credits: leaderboard aggregation by IBM5100's BGrank_bot. Not affiliated with Blizzard
Entertainment.
