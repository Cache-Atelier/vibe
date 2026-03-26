# vibe

Claude Code plugin that lets you actually vibe while Claude works. Curates ambient music and opens a lounge page with embedded players and a countdown timer.

## Install

```shell
# Via the Cache Atelier marketplace
/plugin marketplace add Cache-Atelier/plugins
/plugin install vibe@cache-atelier
```

## Usage

```shell
/vibe
```

Or just ask naturally:

```
put on some music
I need some focus tunes
```

## How it works

1. Claude estimates how long your task will take
2. Picks media from the playlist
3. Generates an HTML lounge page with embedded players
4. Opens it in your browser with a countdown timer
5. Gets to work on your task

## Add your own vibes

Create a JSON file in `vibes/` following `vibes/vibes.schema.json`:

```json
{
  "name": "my-playlist",
  "description": "My custom coding vibes",
  "entries": [
    {
      "title": "Track name",
      "url": "https://www.youtube.com/watch?v=...",
      "embed_url": "https://www.youtube.com/embed/...",
      "platform": "youtube",
      "duration_minutes": null
    }
  ]
}
```

Set `duration_minutes` to `null` for livestreams.

## License

MIT
