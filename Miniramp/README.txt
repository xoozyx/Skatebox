MINI RAMP - a tiny pixel-art skate game (works fully offline)
=============================================================

HOW TO PLAY LOCALLY
  1. Unzip this folder anywhere (keep the folders together).
  2. Double-click index.html (Chrome, Edge, Firefox or Safari).
  No internet, server or install needed: the game code, your character sprites,
  the page background, the window frame and the pixel font are all in this folder.

PRESS F1 IN THE GAME FOR HELP
  The page shows only the game; all controls and tips are in the F1 menu
  (or the ? button in the corner). The game pauses while it is open.
  Esc closes it; Esc again opens the menu (level + outfit).

STARTING AND THE MENU
  The game opens on "PUSH ANY BUTTON TO START": press any key (or tap the game).
  Esc / the MENU button opens the menu: pick the LEVEL and your OUTFIT
  (up/down choose a row, left/right change it, Space or Esc to go back).
  A run in progress is paused; changing the level starts a new run.

QUICK CONTROLS
  Left / Right pump, Up / Down ride toward the back / front
  A flip, D grab, S spin (every 180 turns him around: his back is shown), W near the
  coping = stall / grind / slide

FILES
  index.html ................ the whole game (code, sprites, background and frame are embedded)
  assets/fonts/ ............. Press Start 2P pixel font (SIL Open Font License, see OFL.txt)
  assets/Player_front.png ... front idle animation (4 frames)
  assets/Player_back.png .... back idle animation (4 frames, shown after a 180)
  assets/Background.png ..... page background tile
  assets/Game_window_frame.png ........ the frame you drew (24x24)
  assets/Game_window_frame_ring_256x166.png ... that frame built into the ring around the game window

NOTES
  - The window frame and page background scale in whole-number steps with the
    window, so pixels stay the same size everywhere.
  - Outfit, level and touch-button visibility are saved in the browser's local
    storage on that computer.
  - To use new character sprites, replace the frames in the B64 / B64B lists in
    index.html (24x24 PNGs: 4 front, 4 back), or ask me to do it.
