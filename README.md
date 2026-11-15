# later — Future-Time Ledger & Countdown Dispatcher (`now` Dual)

`later` is the temporal dual of `now`. While `now` records events that have already collapsed into the present (`t <= τ`), `later` versions events, intentions, and scheduled commands in the future (`T > τ`, default offset `+1.00.00 dh36 = +2400 s = +40 min`), backed by Git (`boxC:/home/kof/repos/later.git` & `K0F/later`) and Kof's 50 fps countdown timer [`till`](https://github.com/K0F/till).

## Usage

```bash
# Log an entry to the future ledger (+1.0 dh36 = +40 min ahead by default)
later "otočit magnetofonový pás na vrcholu dekanu"
later "[DRKOTA] vytisknout článek XVII"

# Schedule at a specific Prague time (HH:MM) — logs to later/log, pushes to git,
# and optionally counts down via `till` (-w / --wait) or runs a command (-c)
later -t 06:00 "ranní kontrola 50Hz sítě"
later -t 06:00 -w -c "now '[LATER->NOW] ranní kontrola 50Hz sítě'" "ranní kontrola"

# Inspect future vs. arrived entries in the ledger
later list
```

--τέχνη & kof
