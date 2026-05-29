# Phantoma — Phase 2 Submission Steps

Everything below the line is **prepared and done**. The remaining steps need your
accounts/logins (Unity Play, GitHub, GitHub Pages) — they're spelled out click-by-click.

## ✅ Already done (by Claude)
- **Game code** — 681 lines of hand-written C# (529 net). New this phase: `OrbitCameraRig.cs`
  (mouse-orbit camera), jump in `PlayerController.cs`, `Interactable.cs` + `PlayerInteractor.cs`
  (press-E landmarks). All compile; verified in Play (zero errors).
- **Scene** — `HubScene` wired: camera pivot/orbit, interaction HUD, 4 landmarks. Saved.
- **Website** — `~/Desktop/school-pages-backup/`: root `index.html` + `phase-1/` (Draft, unchanged)
  + `phase-2/` (Final: About, Overview, Blog, Source, GDD), enhanced + build-accurate.
- **GDD PDF** — `phase-2/gdd/Phantoma-GDD-Final.pdf` (linked on the GDD page + root).
- **Website PDFs** — `phase-2/pdf/00-home … 05-gdd.pdf` (all 6 pages).
- **Git** — `~/Desktop/phantoma-unity-v2` is a git repo, committed on `main` (Unity `.gitignore` in place).
- **All 3 builds DONE** in `~/Desktop/phantoma-builds/`: `Mac/Phantoma.app` (133 MB),
  `Windows/` (117 MB), `WebGL/` (28 MB, Unity-Play-ready).

---

## 1. Zip the desktop builds  (builds already produced)
In each of `~/Desktop/phantoma-builds/Mac` and `.../Windows`, delete the
`Phantoma_BurstDebugInformation_DoNotShip/` folder, then zip:
- `Phantoma.app` → `Phantoma-Mac.zip`
- the Windows folder → `Phantoma-Windows.zip`

## 2. Publish WebGL to Unity Play
- Go to **play.unity.com** → sign in → **Publish ▸ Upload a build**.
- Zip the **WebGL** output folder and upload it; set title "Phantoma".
- Copy the public share URL.

## 3. Push the game to GitHub
```
cd ~/Desktop/phantoma-unity-v2
git remote add origin https://github.com/DavidFgamedev/phantoma-unity.git   # create this repo first
git push -u origin main
```
Put the **Mac/Windows zips** on a **GitHub Release** of that repo (or Google Drive) and copy their links.

## 4. Fill the placeholders, then deploy the website
Edit `phase-2/source/index.html` and replace:
- `ADD_UNITY_PLAY_LINK_HERE` → your Unity Play URL
- `ADD_WINDOWS_BUILD_LINK` / `ADD_MAC_BUILD_LINK` → the release/Drive links
- confirm the repo URL is correct

Deploy `~/Desktop/school-pages-backup/` to GitHub Pages:
- **User site:** copy its contents into your `davidfgamedev.github.io` repo, push → live at `https://davidfgamedev.github.io/`
- **Project site:** new repo → push → Settings ▸ Pages ▸ Deploy from `main` `/(root)` → live at `https://davidfgamedev.github.io/<repo>/`
- (Re-run the PDFs only if you change page content — they're already generated.)

## 5. Submit
- **Final website URL:** the Pages URL above (Phase 2 page is `<site>/phase-2/`).
- **PDFs:** `phase-2/gdd/Phantoma-GDD-Final.pdf` (GDD) and the six files in `phase-2/pdf/`.
