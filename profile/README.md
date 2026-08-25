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
| Kotlin | from the repo (Maven Central soon) | [analytics-kotlin-sdk](https://github.com/top-stats/analytics-kotlin-sdk) |
| Ruby | from the repo (RubyGems soon) | [analytics-ruby-sdk](https://github.com/top-stats/analytics-ruby-sdk) |
| Elixir | from the repo (Hex soon) | [analytics-elixir-sdk](https://github.com/top-stats/analytics-elixir-sdk) |
| Swift | Swift Package Manager via the repo URL | [analytics-swift-sdk](https://github.com/top-stats/analytics-swift-sdk) |
| Lua | vendored by the game integrations | [analytics-lua-sdk](https://github.com/top-stats/analytics-lua-sdk) |
| raw HTTP / OTLP | no install — see the [docs](https://docs.topstats.gg) | — |

**Game-server plugins**

| Platform | Status | Repo |
| --- | --- | --- |
| Minecraft (Spigot / Paper) | Available — one jar, 1.8.8 through current | [analytics-minecraft-integration](https://github.com/top-stats/analytics-minecraft-integration) |
| Rust (Oxide / Carbon) | Soon™ | |
| FiveM | Available — drop-in server resource | [analytics-fivem-integration](https://github.com/top-stats/analytics-fivem-integration) |
| Garry's Mod | Soon™ | |
| ARK / Unturned | Soon™ | |
| Discord bots (discord.js) | Available — `npm install @topstats/discord` | [analytics-discord-integration](https://github.com/top-stats/analytics-discord-integration) |

Want one that isn't listed? Tell us in [Discord](https://discord.gg/jjEauJXuZc).

## Contact

- 💬 [Discord](https://discord.gg/jjEauJXuZc)
- 📧 support@topstats.gg
