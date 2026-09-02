# Court's Library

Punk PS2-style AI game maker powered by your own Botpress bot.

## GitHub Pages

This is a static site, so it can be deployed directly with GitHub Pages.

## Botpress connection

Open **BOTPRESS** in the app and enter your public Botpress endpoint. The endpoint is stored only in the browser's localStorage.

Never put a Botpress secret/API key into `index.html` or any public GitHub Pages file.

### Expected Botpress response

For the best experience, have your bot return JSON in this shape:

```json
{
  "message": "Game generated.",
  "files": {
    "index.html": "<canvas id=\"game\"></canvas>",
    "style.css": "body { margin: 0; background: #111; }",
    "game.js": "console.log('hello');"
  }
}
```

The app also accepts plain-text responses and displays them in the AI chat.

## Next planned pieces

- Persistent projects
- Better multi-file editor
- Asset importing and packaging
- Botpress-specific response adapter
- ZIP export
- More built-in game templates
- Custom Court's Library GIFs and sounds
