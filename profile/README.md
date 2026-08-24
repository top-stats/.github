<h1 align="center">TopStats</h1>

<p align="center">
  <b>Product analytics for backends, bots, and game servers.</b><br>
  Send events over HTTP, OpenTelemetry, or an SDK — get funnels, retention,
  live dashboards, and behavioral alerts.
</p>

<p align="center">
  <a href="https://topstats.gg">Website</a> &nbsp;·&nbsp;
  <a href="https://docs.topstats.gg">Docs</a> &nbsp;·&nbsp;
  <a href="https://bots.topstats.gg">Bot analytics</a> &nbsp;·&nbsp;
  <a href="https://discord.gg/jjEauJXuZc">Discord</a>
</p>

---

## What we build

[**topstats.gg**](https://topstats.gg) — schema-agnostic event analytics built
for server-side data. No fixed schema to design up front: send whatever
properties you have and query them later.

- **Live dashboards** — widgets update in near real time as events land.
- **Funnels, retention, and segments** — behavioral analysis over your own events.
- **Actors** — attribute events to a player, user, or server.
- **Alerts and digests** — get told when a metric moves, on a schedule or on a threshold.
- **Sharing and embedding** — public dashboards and embeddable widgets.
- **Flat, volume-based pricing** — free plan included, no card required.

[**bots.topstats.gg**](https://bots.topstats.gg) — historical growth, vote
trends, and rankings for tens of thousands of Discord bots listed on top.gg.
Independent, not affiliated with top.gg.

## Sending events

One endpoint, no SDK required:

```bash
curl -X POST https://topstats.gg/v1/events \
  -H "Authorization: Bearer $TOPSTATS_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"name":"player_join","properties":{"map":"dust2"},"_actor":"user_123"}'
```

Already running OpenTelemetry? Point any OTLP SDK or Collector straight at us.
Full details in the [docs](https://docs.topstats.gg).

## SDKs

Every SDK sends the same payload as the HTTP API above. Repos land under this
org as they ship.

**Available today**

| Language | Install | Repo |
| --- | --- | --- |
| Node.js / JavaScript / TypeScript | `npm install @topstats/analytics` | [analytics-node-sdk](https://github.com/top-stats/analytics-node-sdk) |
| Python | from the repo (PyPI soon) | [analytics-python-sdk](https://github.com/top-stats/analytics-python-sdk) |
| Go | `go get github.com/top-stats/analytics-go-sdk` | [analytics-go-sdk](https://github.com/top-stats/analytics-go-sdk) |
| PHP | from the repo (Packagist soon) | [analytics-php-sdk](https://github.com/top-stats/analytics-php-sdk) |
| Rust | from the repo (crates.io soon) | [analytics-rust-sdk](https://github.com/top-stats/analytics-rust-sdk) |
| C# / .NET | from the repo (NuGet soon) | [analytics-csharp-sdk](https://github.com/top-stats/analytics-csharp-sdk) |
| Java | from the repo (Maven Central soon) | [analytics-java-sdk](https://github.com/top-stats/analytics-java-sdk) |
| raw HTTP / OTLP | no install — see the [docs](https://docs.topstats.gg) | — |

**Soon™**

| | | |
| --- | --- | --- |
| Kotlin | Ruby | Elixir |
| Swift | Unity | Unreal |
| Godot | | |

**Game-server plugins — Soon™**

| Platform | Target |
| --- | --- |
| Minecraft | Spigot / Paper |
| Rust | Oxide / Carbon |
| FiveM | GTA RP resource |
| Garry's Mod | GLua addon |
| ARK / Unturned | Survival mod |

Want one that isn't listed? Tell us in [Discord](https://discord.gg/jjEauJXuZc).

## Contact

- 💬 [Discord](https://discord.gg/jjEauJXuZc)
- 📧 support@topstats.gg
