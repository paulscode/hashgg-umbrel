# HashGG Community App Store

An [Umbrel](https://umbrel.com) community app store for [HashGG](https://github.com/paulscode/hashgg).

## Apps in this store

### HashGG

Sovereign hash routing for your Bitcoin miners. Exposes your [Datum Gateway](https://github.com/ocean-xyz/datum_gateway) stratum port to the public internet via [playit.gg](https://playit.gg) or an SSH tunnel to a VPS you control — so any miner, anywhere, can connect to your node and mine blocks *you* built.

Requires the official [**Datum**](https://apps.umbrel.com/app/datum) Umbrel app (which in turn requires the **Bitcoin Knots** app).

## How to add this store to your Umbrel

1. Open your Umbrel dashboard.
2. Go to **App Store**.
3. Click the ellipsis (⋯) in the upper-right, then **Community App Stores**.
4. Paste the URL of this repo:
   ```
   https://github.com/paulscode/hashgg-umbrel
   ```
5. Click **Add**.
6. The **HashGG Community App Store** now appears under its own heading in the App Store.
7. Install **Datum** first (from the official store) if you haven't already, then install **HashGG** from the community store.

## Support

- HashGG issues: https://github.com/paulscode/hashgg/issues
- Umbrel (general): https://community.umbrel.com

## License

MIT — see [LICENSE](LICENSE).

## Notes

- **Architecture:** the HashGG container image is published multi-arch (linux/amd64 + linux/arm64). The arm64 build has not been hardware-tested on Raspberry Pi; please report issues if you hit any.
- **Datum dependency:** HashGG relies on Datum exposing its stratum port at `datum:23334` inside the Umbrel network (or via `APP_DATUM_NODE_IP` env export). If a future Datum release breaks this, open an issue.
