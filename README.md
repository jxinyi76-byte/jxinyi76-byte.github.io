# YUKI JIANG Portfolio — SunBiscuit Interactive Edition

## 先解压，再打开

不要在 WinZips/压缩包预览窗口中直接双击 HTML。请先点击“全部解压/一键解压”，保持 `index.html`、`YUKI_JIANG_Portfolio.html` 与 `assets` 文件夹处于同一层级，然后打开 `index.html`。

## Contents
- `index.html` — 推荐打开的作品集入口。
- `YUKI_JIANG_Portfolio.html` — 与入口内容相同的主文件，便于替换原网站文件。
- `assets/sunbiscuit/` — SunBiscuit 纸箱纹理、锡纸包装与六种口味贴纸素材。
- `assets/pinfenghuang/` — “品奉凰”品牌全案的 9 张原始横版展板，按封面、前言、规范与应用顺序整理。
- `assets/board/studio-workspace.webp` — 首页 Projects 拍立得卡片的新工作室照片。
- `assets/picture-book/` — optimized JPEG exports from the supplied picture-book archive (cover, pages 03–32, back cover).
- `assets/magazine/` — optimized JPEG exports of the 17 supplied editorial spreads.
- `ASSET_MANIFEST.json` — original filenames, page numbers, and source dimensions.

## Open locally
1. Extract the ZIP while keeping the `assets` folder beside `index.html` and `YUKI_JIANG_Portfolio.html`.
2. From this folder, start a local static server:
   - Python: `python -m http.server 5173`
   - Or use VS Code Live Server.
3. Open `http://localhost:5173/index.html`.

The existing portfolio already uses CDN-hosted Tailwind CSS, Font Awesome, and Google Fonts, so an internet connection is needed for those existing external resources. The two new viewers and their image assets do not add a new JavaScript library dependency.

## Integration and interaction
- Packaging: three square SunBiscuit boxes retain their original textures and 360° drag rotation. Clicking a box centers it and opens four independent top flaps around their real fold axes. The vacuum pouch shares the box's current 3D coordinate system and rises along its own opening axis. In the dedicated pouch view, only the red flavour information block peels away, exposing yellow adhesive backing; the removed sticker can be dragged anywhere on screen and reattached with the reset button. Six high-resolution flavour labels remain switchable from the top controls.
- Brand identity: the existing `p1` window now reveals a softly blurred “品奉凰” cover. Clicking it opens a native Scroll Stack presentation based on the supplied React Bits reference: each wheel step introduces the next full artwork while earlier cards remain as a scaled, dimmed, lightly blurred deck with a 26px visual peek. All nine supplied boards are shown uncropped and in their original content order.
- The existing `p2` / “绘本设计” work window now opens the picture-book viewer.
- The existing `p4` / “版式设计” work window now opens a dedicated Cursor Image Trail presentation.
- Picture book: the original cover first appears as a dimensional floating closed book. Clicking it—or scrolling down—opens it into a flat two-page spread without changing any artwork. Continued wheel input turns spreads forward or backward; click zones, keyboard arrows, page-turn sheets, shadows, and return controls remain available. Interior pages stay paired in order (03–04, 05–06, …, 31–32), followed by the original back cover.
- Editorial: the viewer starts as a blank paper window. When the pointer enters the page, the magazine content appears. Horizontal mouse position continuously selects and smoothly moves to the corresponding supplied spread; the active spread is emphasized while neighboring spreads recede. Wheel and arrow controls remain as fallbacks.

## Important reference note
The supplied BookBlock URL is a page-flip plugin reference. The supplied CodePen URL currently resolves to **“GSAP Cursor Trailer Effect”**, not a clearly identifiable magazine browsing/page-motion example. Therefore the editorial viewer implements a usable horizontal mouse/drag-controlled browsing experience for the provided spreads, but it should not be described as an exact reproduction of that CodePen. If exact matching to a different magazine interaction was intended, provide the correct CodePen URL and the interaction can be aligned to it.

## Validation performed
- JavaScript syntax checked with Node.js `--check`.
- Verified all local asset references in the HTML exist.
- Verified all generated image files can be decoded.
- Confirmed the project has no `package.json` or framework build step; it is an existing standalone HTML site.
- Visual browser QA confirmed: sealed box faces no longer expose a ring gap; the enlarged local-axis pouch emerges above the four open flaps; the dedicated pouch has a thinner, tapered foil side profile; the “品奉凰” Scroll Stack advances by mouse wheel with counter/progress feedback; the supplied studio photo appears in the Projects Polaroid; picture-book and editorial viewers remain intact.
