# How to add or edit a project on your website

Everything lives in `index.html`. You do NOT need to touch the HTML layout.

## 1. Add a project
Open `index.html`, find the line `const PROJECTS = [` (near the bottom, in the last <script>).
Copy one existing `{ ... }` block, paste it, and edit the fields:

```js
{
  num: '09',                       // any label/number shown on the card
  name: 'My New Project',
  desc: 'One paragraph. You can use <strong>bold</strong>.',
  stack: ['Python', 'FastAPI', 'React'],   // tech tags
  link: 'https://github.com/you/repo',     // demo or repo URL ('' hides the button)
  media: ['media/myproj-1.png', 'media/myproj-demo.gif'],  // [] for none
  highlight: false                 // true = accent-outlined card
}
```

## 2. Add media (images / GIFs)
1. Drop the image or GIF into the `media/` folder.
2. List its path in that project's `media: [...]`.
Thumbnails appear on the card; clicking one opens a full-screen viewer
(arrow keys / on-screen arrows to move between images, Esc to close).

## 3. Save and publish
Commit and push (GitHub Pages redeploys automatically):
```
git add . && git commit -m "Add project X" && git push
```

Tip: keep images reasonably small (under ~500 KB) so the page stays fast.
