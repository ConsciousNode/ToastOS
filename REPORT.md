# ToastOS — Build Report

## What's in it
- `toastos.html`: A single-file, zero-dependency, MIT-licensed graphical OS running inside a top-down chrome toaster.
- **Hardware & Boot**: Clickable toaster lever that boots the slice out of the slot with a Web Audio synthesized *ding* and toast-themed POST log (`Mounting /dev/crumb... OK`, `Calibrating butter... OK`), plus lever-triggered eject/reboot to a fresh pale slice.
- **Browning Clock & Balanced Ternary Dial (`T / 0 / 1`)**: Continuous browning from Pale to Golden (`35%–75%`) to Dark to Burnt (`90%+`, triggering falling crumb particles and a warning banner). The rotary dial switches between `T` (`-1 Frozen`, icy window corners, frost overlay, sluggish window drag, slower sequencer), `0` (`0 Bread`), and `1` (`+1 Toast`, faster browning and brisker tempo).
- **Window Manager**: Draggable, stackable, minimizable, and closable windows bounded to the crumb surface inside the crust bezel.
- **Six Usable Apps**:
  1. **Butter Paint**: Canvas smear painting with Butter, Strawberry Jam, Marmalade, and Yeast Spread (generic name used to avoid real trademarks), plus save-to-disk.
  2. **Crumb Explorer**: Browse, open, create, and delete `.crumb`/`.toast`/`.txt` files and saved paintings, with a **Crumb Tray** you empty by clicking **Shake Tray** (shakes the toaster with synthesized rattle audio).
  3. **Toaster Terminal**: Interactive shell with 14 commands (`help`, `ls`, `cat`, `touch`, `echo`, `rm`, `shake`, `brown`, `dial`, `butter`, `eject`, `whoami`, `uname`, `clear`) and up/down command history.
  4. **Jam Session**: 4-track × 8-step sequencer using clickable jam dots and Web Audio synthesis.
  5. **Breadit**: Invented sandwich social feed with Toast/Soggy voting and local posting.
  6. **Settings**: Bread type (`White`, `Rye`, `Sourdough`, `Pumpernickel` procedural crumb textures), crust bezel thickness slider, ternary dial sync, and storage reset.

## What works
- All six apps, the window manager, procedural bread textures, continuous browning, falling burnt crumbs, Web Audio synthesis (boot ding, eject spring, dial clicks, tray shake, step sequencer), and `try/catch`-wrapped `localStorage` persistence.

## What doesn't (honest limitations)
- **Window resizing**: Windows can be dragged, stacked, minimized, and closed, but do not have corner/edge resize handles.
- **Individual window crumb accumulation**: At `90%+` burnt, falling crumb particles rain across the entire bread screen and over windows, rather than sticking permanently to individual window titlebars.
- **Breadit networking**: Breadit is strictly local and offline; posts and votes are stored in `localStorage` with no remote server.

## The toast-related decision I'm proudest of
Making **Golden Toast (`35%–75%` browning)** and the **Balanced Ternary Dial (`T / 0 / 1`)** genuinely alter how apps behave rather than being purely cosmetic: Butter Paint spreads wider and smoother on golden toast, Jam Session switches its synth voice to warmer triangle harmonics during the golden groove, and flipping the dial to `T` (`-1 Frozen`) physically slows down window dragging and sequencer tempo while frosting the window corners.
