# ToastOS: a graphical operating system that runs inside a single slice of toast

ConsciousNode SoftWorks goof build. Xinu rules: one self-contained HTML file, zero external dependencies, works offline, MIT licensed. This is for fun. Make it delightful, weird and committed to the bit.

## The premise
A full desktop operating system whose screen is a slice of bread, shown in a toaster from above. The bread *is* the display. Everything about the OS is shaped by being toast.

## What to build
1. **The device.** A chrome toaster seen from above, with one slot. Inside the slot is a slice of bread, and the bread is the screen: windows, icons and a taskbar drawn on the crumb. The crust is the screen bezel.
2. **Boot.** Press the toaster lever to boot. The bread rises out of the slot with a *ding*, made with Web Audio, no files. Boot messages are toast-themed ("Mounting /dev/crumb… OK", "Calibrating butter… OK").
3. **Browning is the clock.** The longer the OS runs, the more the bread browns, from pale through golden to dark. Browning is a visible, continuous system state: some apps run better on golden toast, and at "burnt" the OS starts dropping crumbs (stray pixels) and warns you. Pushing the lever again ejects the slice, which is a reboot, and you get a fresh pale slice.
4. **Three toast settings, in balanced ternary**, on a dial on the toaster: **−1 Frozen** (everything runs slow and frosty, with ice crystals on the windows), **0 Bread**, **+1 Toast** (fast, warm, browns quicker). Show the setting as T / 0 / 1.
5. **Apps** (at least 6, all actually usable):
   - **Butter Paint**: paint with spreads (butter, jam, marmalade, vegemite) that smear when you drag.
   - **Crumb Explorer**: a file browser where files are crumbs. Delete sends them to the Crumb Tray, which you can empty by shaking (a button).
   - **Toaster Terminal**: a working command line with at least 10 real commands (`ls`, `cat`, `butter`, `eject`, `brown`, `help`…).
   - **Jam Session**: a tiny step sequencer whose notes are jam dots.
   - **Breadit**: a fake social feed of posts by sandwiches. All content is clearly invented and bread-themed. No real people, no real brands.
   - **Settings**: crust thickness, bread type (white, rye, sourdough, pumpernickel) that changes the screen texture, and the toast dial.
6. **Window manager.** Drag, close and stack windows. Windows sit on the bread surface and get crumbs on them as browning rises.
7. **Persistence.** Saved paintings and files go in localStorage, wrapped in try/catch so the OS still runs if storage is missing.

## Rules
- Draw everything with canvas or SVG and generate every sound with Web Audio. No images, fonts or files from the network.
- No real trademarks, products, brands or people anywhere.
- If a feature doesn't work, say so in REPORT.md and leave it out. Don't fake it. Short honest notes beat long claims.

## Deliver
- `toastos.html` (the whole thing)
- `REPORT.md`: what's in it, what works, what doesn't, and the toast-related decision you're proudest of.
