# 🌸 Send a Bouquet

Send someone flowers that bloom. Type their name, add a note, share the link. It opens into a 3D lily bouquet made entirely of text characters, with music.

Nothing is stored anywhere. The name and note live only inside the link you share. You can also make a heart-shaped QR code to print or put on a gift.

## How it works

- **The flowers:** 13 lilies, each made of six curved, folded petals in 3D. They open from buds, turn toward the viewer and sway. Everything is drawn on a hidden canvas every frame.
- **The ASCII look:** a WebGL shader turns that hidden picture into a grid of coloured characters, where brighter cells get denser characters. There is a Canvas 2D fallback.
- **Link previews:** a small serverless function (`api/for.js`) adds "A bouquet for [name] 🌸" to each link (`/f?t=Name&f=From&n=Note`), so WhatsApp and iMessage show the name in the preview.
- Plain HTML, CSS and JavaScript. No framework, no build step.

## Run it locally

```bash
npm i -g vercel
vercel dev
```

Run the tests with `node --test tests/for.test.js`.

## Deploy

Import this repo on [Vercel](https://vercel.com/new). No settings needed.
After deploying, replace `YOUR-SITE` and `YOUR-USERNAME` in `index.html` with your Vercel domain and GitHub username.

## Credit

This project is based on [ASCII Bouquet](https://github.com/Devansh-Singhal/send-a-bouquet) by Devansh Singhal, used under the MIT license. The idea, the bouquet renderer and the design come from his work. The original copyright notice is kept in [LICENSE](LICENSE).

## License

MIT. See [LICENSE](LICENSE).
