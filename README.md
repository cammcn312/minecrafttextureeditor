# ⛏ Texture Studio

A tiny offline texture editor for Minecraft Java Edition. No install, no admin rights, no internet needed (except the optional AI helper).

## Run it
1. Download this folder. Keep `index.html` and `jszip.min.js` together.
2. Double-click **index.html** (opens in **Chrome or Edge**).
3. Click **1. Pick Minecraft folder** and choose your `.minecraft` folder:
   - Windows: press `Win+R`, type `%appdata%\.minecraft`, copy that path into the picker's address bar.
   - Mac: in the picker press `Cmd+Shift+G` and paste `~/Library/Application Support/minecraft`.
   - Other launchers: use **…or load client.jar** and pick `versions/<version>/<version>.jar`.
4. Pick a block/item/entity on the left, paint, then **2. Save to Minecraft**.
5. In Minecraft: *Options → Resource Packs* → move your pack to the right-hand list → Done. (F3+T reloads in-game.)

## Is it safe?
- It runs in the browser sandbox and can only touch the one folder you pick.
- It **only reads** `client.jar` and **only writes** `resourcepacks/<Pack Name>.zip`. It never edits game files.
- It refuses to overwrite a pack it didn't make. Delete the zip to undo everything.
- No Minecraft assets are included here; textures are read from your own copy of the game.

## Features
Asset browser (Blocks / Items / Entities / More) with search · pencil, eraser, fill, fill-all-matching, picker, mirror, brush size · hue/saturation/brightness recolour · layers & overlays (from blank, from another game texture, or from a PNG) · undo/redo · new textures · re-opens your earlier pack · AI idea helper.

## AI Idea Helper
Needs internet and an Anthropic API key (paste it once via "Set key"; stored only in this browser). Uses a small, cheap model (`MODEL` at the top of the script). Colours it suggests are clickable.

## Limits
- Resource packs can only retexture things the game already has. A brand-new texture needs a model to appear in-game.
- Entity textures are flat skin sheets (no 3D preview).
- Firefox/Safari can't write folders: use **load client.jar**; Save then downloads a zip to drop in `resourcepacks`.
