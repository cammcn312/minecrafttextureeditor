# ⛏ Texture Studio

Paint your own Minecraft Java blocks, items and mobs, then see them in your game. Works offline in Chrome or Edge. Nothing to install.

## For the kid
1. Double-click **index.html** (opens in Chrome or Edge).
2. Click **🔍 Find my Minecraft**. A window opens and the address is already copied: press **Ctrl+V**, **Enter**, open the folder with the biggest number (like `26.3`), pick the file ending in **.jar**. (Only the first time. It remembers.)
3. Pick something on the left, paint it, press the big green **🎮 Put in Minecraft!** button.
4. Follow the pop-up: in Minecraft go to **Options → Resource Packs**, drag the saved zip onto the game window, click the ▶ arrow.

A yellow bar at the top always says what to do next. 🎲 **Surprise me!** (Ideas tab) gives colour themes with no internet.

## For the grown-up
- The whole app is the single file `index.html` (JSZip is built in; its licence is in `JSZIP-LICENSE.md`). You can copy just that one file anywhere.
- There is no folder picker (Chrome blocks `.minecraft`). The app reads only the game's `.jar` file that he picks, and caches it in the browser.
- **Optional one-time automatic saving:** Chrome/Edge refuse to let websites write inside `.minecraft`, so the app uses a Windows "junction" (a shortcut folder). After the first save press *⚡ Grown-up: make this automatic* (or ⚙ → Set up automatic saving). It copies one command: press **Win+R**, paste, Enter (a black window should say "Junction created"). That makes `%userprofile%\TextureStudio` appear inside `.minecraft\resourcepacks`. Then choose that `TextureStudio` folder in the app. From then on the green button saves straight in; he only presses F3+T in-game. (Mac: the same idea with `ln -s`, shown in the app.) The app only writes to that folder if it is empty or already its own.
- **⚙ Grown-ups corner:** game file, automatic saving, AI key, forget saved pictures.
- **AI Idea Helper chat** needs internet and an Anthropic API key (⚙ → Set key; stored only in this browser). Everything else works without it.
- If an installation uses a custom game directory, save the pack into that folder's `resourcepacks`.

## Safety
- Runs in the browser sandbox and can only touch folders you pick.
- Only **reads** the game `.jar` he picks; only **writes** the one pack zip. Never edits game files.
- Refuses to overwrite a pack it didn't make. Delete the zip to undo everything.
- Work is autosaved in the browser, so closing the tab doesn't lose it. Undo, redo and "start this picture again" are always there.
- No Minecraft assets are included; textures are read from your own copy of the game.

## Making a brand-new item
**✨ Make something new** → paint → save. The pack also gets the model files and the save screen shows a command like
`/give @s minecraft:paper[item_model="minecraft:ruby"]`. Reload the pack (F3+T), paste it in chat (cheats on) and you're holding it. Needs Minecraft 1.21.4+. New blocks become holdable cubes (not placeable).

## Limits
- Packs can only retexture what the game has; new items use the `item_model` trick above.
- 3D preview: blocks, items, creeper and zombie/skeleton-style mobs only.
- Firefox/Safari: no automatic saving; use the drag-and-drop way.
