# ⛏ Texture Studio

Paint your own Minecraft Java blocks, items and mobs, then see them in your game. Works offline in Chrome or Edge. Nothing to install.

## For the kid
1. Double-click **index.html**.
2. Click **🔍 Find my Minecraft**. Paste the address it shows into the window that pops up, press Enter, then **Select Folder**.
3. Pick something on the left, paint it, and press the big green **🎮 Put in Minecraft!** button.
4. In Minecraft: **Options → Resource Packs**, click the ▶ arrow on *My Textures*.

A yellow bar at the top always says what to do next. 🎲 **Surprise me!** (Ideas tab) gives colour themes with no internet.

## For the grown-up
- Keep `index.html` and `jszip.min.js` together.
- **Chrome says "Can't open this folder"?** Use the *backup way* on the welcome screen: pick the game's `.jar` file (under `.minecraft/versions/<version>/`). Saving then downloads a zip and shows how to move it into `resourcepacks`. Optionally pick the `resourcepacks` folder so saving goes straight in.
- **⚙ Grown-ups corner:** Minecraft version, pack name, resourcepacks folder, and the AI chat key.
- **AI Idea Helper chat** needs internet and an Anthropic API key (⚙ → Set key; stored only in this browser). Without it everything else works.
- If an installation uses a custom game directory, save to that folder's `resourcepacks`.

## Safety
- Runs in the browser sandbox and can only touch folders you pick.
- Only **reads** `client.jar`; only **writes** `resourcepacks/<Pack Name>.zip`. Never edits game files.
- Refuses to overwrite a pack it didn't make. Delete the zip to undo everything.
- Work is autosaved in the browser, so closing the tab doesn't lose it. Undo, redo and "start this picture again" are always there.
- No Minecraft assets are included; textures are read from your own copy of the game.

## Making a brand-new item
**✨ Make something new** → paint → save. The pack also gets the model files and the save screen shows a command like
`/give @s minecraft:paper[item_model="minecraft:ruby"]`. Reload the pack (F3+T), paste it in chat (cheats on) and you're holding it. Needs Minecraft 1.21.4+. New blocks become holdable cubes (not placeable).

## Limits
- Packs can only retexture what the game has; new items use the `item_model` trick above.
- 3D preview: blocks, items, creeper and zombie/skeleton-style mobs only.
- Firefox/Safari can't save into folders; use the backup way.
