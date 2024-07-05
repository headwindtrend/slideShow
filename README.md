# slideShow
a slideshow feature in html

- can `Choose Folder` to use all image files in that folder for the slideshow.
- can `Choose Files` to select multiple image files in a folder for the slideshow.
- use spacebar or mouseclick to play/pause.
- use left/right arrows to force moving backward/forward respectively. this works no matter it's in play/pause mode.
- click the index number, located at the top-right corner, to toggle between chronological order and random order. when it's in random order, a red border is shown around the index number whereas no border is shown when it's in chronological order. remark: since the pool size (how many images are loaded) too low (typically, one or zero) can cause problem to the code (and random order for 2 images is meaningless), i added a checking that this toggle will only work when the pool size is bigger than 2.

Change log:

* Jul 5, 2024&nbsp;&nbsp;&nbsp;&nbsp;cosmetic tweaks: the "loader" controls were always shown. from now on, they will be hidden in "play" mode, and shown only in "pause" mode. the "index number" control on the other hand, with some flexibility, yet still can be hidden if necessary. a rightclick on it can dismiss it. and, "pause" mode will bring all controls back (shown), including "index number".

* Jul 3, 2024&nbsp;&nbsp;&nbsp;&nbsp;added a random order feature; and bug fixes.
