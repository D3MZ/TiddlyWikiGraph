# TiddlyWikiGraph

Single-file TiddlyWiki prepared for GitHub Pages and the built-in GitHub saver.

## Local editing

```bash
npm install
npm start
```

Open http://127.0.0.1:8080. Local server edits are saved as tiddler files under `wiki/tiddlers/`.

## Build `index.html`

```bash
npm run build
```

This writes the single-file wiki to `./index.html`. GitHub Pages can serve this directly from the repository root.

## GitHub Pages setup

1. Push this repo to GitHub.
2. In the GitHub repo, go to Settings → Pages.
3. Set source to `Deploy from a branch`.
4. Choose branch `main`, folder `/root`.
5. Visit `https://YOUR_USERNAME.github.io/YOUR_REPO/`.

## Browser saving back to GitHub

TiddlyWiki can save the live `index.html` back to GitHub using its built-in GitHub saver.

In the online wiki, open Control Panel → Saving → Git Service Saver / GitHub Saver and fill:

- Username: your GitHub username
- Password: a GitHub personal access token
- Repository: `owner/repo`
- Branch: `main`
- Path: `/`
- Filename: `index.html`

Use a fine-grained token limited to this repo with contents read/write permission. The token is stored in browser local storage, so avoid shared machines.

## Graph layer

Start simple: use normal TiddlyWiki links and tags as graph edges. Then add either a TiddlyWiki graph plugin or a custom Cytoscape/D3 tiddler to visualize them.
