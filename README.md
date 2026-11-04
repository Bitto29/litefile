# LiteFile

A lightweight, dark-mode document library for your Scribd embeds. It is plain HTML, CSS, and JavaScript. There is no framework, database, login, build step, or external font dependency.

## Add a document

1. Open `documents.js` in this repository.
2. Find the `window.LITEFILE_DOCS` array.
3. Copy the example object in the comment at the bottom of the file.
4. Paste it after the last document object. Add a comma after the previous object.
5. Change the id, title, folder, and embedUrl values.
6. In Scribd's iframe embed code, copy the URL inside the iframe src attribute and paste it as embedUrl.
7. Commit the edit. The updated list will appear on the site after deployment.

Every different folder value creates a folder automatically. Keep each id unique.

## Deploy with GitHub Pages

Open repository Settings → Pages. Choose Deploy from a branch, select main and /(root), then save.

## Performance and limitations

The library has no heavy dependencies and loads only the selected document's iframe. Scribd still hosts and serves the actual viewer and PDF pages, so LiteFile cannot fix slow Scribd servers or inaccessible documents. Use Open on Scribd as a fallback.

Favourites are saved locally in the current browser/device. The document list itself lives in documents.js and is shared by visitors.