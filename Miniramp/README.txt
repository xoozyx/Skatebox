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

EDITING THE LEVEL ART (assets/levels/)  -  levels: BIG RAMP and SEWER (the half-size ramp)
  Each level is two PNG layers, both 240x138 pixels (the game screen above the score bar).
  The game draws them in this order: background -> ramp -> skater -> score bar.

    big_background.png   sewer_background.png   the scene behind the ramp (beach: sky, hill, fence, crowd; sewer: brick tunnel, pipes, ooze)
    big_ramp.png         sewer_ramp.png         the ramp itself: deck, riding surface, front face,
                                               coping pipes, props. Transparent where there is no ramp.

  Edit any of them in your pixel editor and save over the file (keep the name and 240x138 size).
  Reload index.html (Ctrl+F5) and the game uses your picture instead of the built-in drawing.
  Delete a file to go back to the built-in drawing for that layer. Each file is optional.

  Reference files (the game does not load these):
    big_guide.png  sewer_guide.png     transparent overlays for your editor. Magenta = the line his
                                      wheels ride on, yellow dots = front/back edge of the riding
                                      surface (depth), cyan crosses = the coping points where stalls
                                      and grinds happen, orange ticks = where he launches off the lip.
    big_full_preview.png  sewer_full_preview.png    both layers together, as the game shows them.

  IMPORTANT: the shape of the ramp is also in the game's physics. You can repaint everything
  (colours, textures, decks, pipes, scenery) but if you move the riding curve or the coping the
  skater will no longer sit on your drawing - use the guide overlays to keep them in line.
  The game's palette is #071821, #42463f, #a9bb9c, #e0f8cf (other colours work too).

FILES
  index.html ................ the whole game (code, sprites, background and frame are embedded)
  assets/levels/ ............ the level art layers and guides (see above)
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
