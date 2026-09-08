# JellySpotlight Plugin Repository

Add this URL under **Dashboard → Plugins → Repositories**:

```text
https://raw.githubusercontent.com/skijk/jellyfin-plugin-jellyspotlight-repository/main/manifest.json
```

Version 0.4.0.0 and later require Jellyfin 12.0 and File Transformation 3.0.
Jellyfin 10.11 servers must use the retained 0.3.x releases. The manifest keeps
both ABI generations so Jellyfin can select a compatible version.

## Dependencies

| Component | Status | Used for |
| --- | --- | --- |
| Jellyfin 12.0 | Required | Supported server and web client |
| File Transformation 3.0 | Required | Loads the Spotlight web assets |
| Jelana | Required | Supplies hourly cached analytics rows |
| Playback Reporting | Transitive | Required by Jelana; Spotlight never queries it directly |
| Arr Watch | Optional | Supplies movies and season premieres for **Coming soon** |
| JellyBulletin | Optional | Keeps deterministic placement around bulletin panels |

Install File Transformation, Playback Reporting and Jelana before JellySpotlight.
If an optional provider is unavailable, its row or placement integration is skipped
without affecting the other Spotlight rows.
