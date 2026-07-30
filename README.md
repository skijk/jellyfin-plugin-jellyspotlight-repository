# JellySpotlight Plugin Repository

Add this URL under **Dashboard → Plugins → Repositories**:

```text
https://raw.githubusercontent.com/skijk/jellyfin-plugin-jellyspotlight-repository/main/manifest.json
```

## Dependencies

| Component | Status | Used for |
| --- | --- | --- |
| Jellyfin 10.11.11 | Required | Supported server and web client |
| File Transformation | Required | Loads the Spotlight web assets |
| Jelana | Required | Supplies hourly cached analytics rows |
| Playback Reporting | Transitive | Required by Jelana; Spotlight never queries it directly |
| Radarr Watch | Optional | Enables the **Coming soon** source |
| JellyBulletin | Optional | Keeps deterministic placement around bulletin panels |

Install File Transformation, Playback Reporting and Jelana before JellySpotlight.
If an optional provider is unavailable, its row or placement integration is skipped
without affecting the other Spotlight rows.
