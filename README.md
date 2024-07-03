# slideShow
a slideshow feature in html

- can `Choose Folder` to use all image files in that folder for the slideshow.
- can `Choose Files` to select multiple image files in a folder for the slideshow.
- use spacebar or mouseclick to play/pause.
- use left/right arrows to force moving backward/forward respectively. this works no matter it's in play/pause mode.
- click the index number, located at the top-right corner, to toggle between chronological order and random order. when it's in random order, a red border is shown around the index number whereas no border is shown when it's in chronological order. remark: since the pool size (how many images are loaded) too low (typically, one or zero) can cause problem to the code (and random order for 2 images is meaningless), i added a checking that this toggle will only work when the pool size is bigger than 2.

2024.07.03 - added a random order feature; and bug fixes.
