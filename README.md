# Simple Slideshow

This is a simple slideshow application that allows users to view images in a slideshow format. Users can load images from their local files or folders (get images by dragging from a webpage is also possible) and navigate through the images using keyboard/mouse/touch controls. The updated version includes a thumbnails panel for easier navigation and additional features for managing images.

## Features

- Load images from local files or folders
- Navigate through images using keyboard/mouse/touch controls
- Play and pause the slideshow
- Exclude images from the slideshow
- Random order playing
- Thumbnails panel for easier navigation
- Drag and drop images to reorder or remove them
- Display image index numbers
- Resize thumbnails using mouse wheel or slider

## How to Use

1. Open the `slideShow.html` file in your web browser.
2. Click on `Choose Folder` or `Choose Files` to load images.
3. Use the following keyboard/mouse/touch controls to navigate through the slideshow:
   - Space/Click: Play/Pause the slideshow
   - Arrow Right: Show the next image
   - Arrow Left: Show the previous image
   - Rightclick: Dismiss the index number << rightclick on the index number (located at the top-right corner)
   - F2: Toggle the thumbnails panel
   - Mouse-wheel/Touch-slide: Resize the thumbnails << mouse-wheel on (or touch-slide from) the `dark spot` control
4. Click on `Exclude` to remove the current image from the slideshow.
5. Click on the index number (located at the top-right corner) to toggle random order playing.
6. Click on the `green spot` control to open the thumbnails panel. (Click on the `dark spot` control to close the thumbnails panel.)
7. Drag and drop images within the thumbnails panel to reorder or remove them.
8. Click on an image in the thumbnails panel to jump to it in the slideshow. (This also close the thumbnails panel and enters pause-mode.)
9. Use the mouse wheel or "touch slider" to resize thumbnails. (Note: the touch-slider is "invisible", just slide from the `dark spot` to see)

## Thumbnails Panel

The thumbnails panel provides an overview of the images included in the slideshow. You can reorganize them by drag and drop to change their sequential order, insert new images, and remove images. You can also jump to a particular image by clicking on its thumbnail.

### Reordering Thumbnails

Moving a thumbnail (changing the sequential order of the loaded images) through drag and drop is intuitive. To move a thumbnail to the end or top of the list, drag and drop it on itself where the pointer lands on the bottom-right corner (to move it to the end) or the top-left corner (to move it to the top). This is especially helpful when the target end is far away. (Note: the definition of the "corners" in proximity is one third of width times one third of height.)

### Inserting Images

Insert images by dragging them from a webpage or file explorer and dropping them at the desired point in the list. To insert at the top or bottom of the list, land the image on the empty space (green background). Landing on the lower half of the panel inserts it at the end, while the upper half inserts it at the top. (Note: while this drag&drop allows you to place the payload at the desired point, the drag&drop on the slideshow (not the thumbnails panel) remains appending the payload at the end.)

### Removing Thumbnails

Remove (aka "exclude") a thumbnail by dragging and dropping it to the empty space (green background).

### Scrolling

A single click on the empty space (green background) can scroll the list to the top or bottom, depending on whether the click is on the upper or lower half of the panel.

### Resizing Thumbnails

The percentage shown in the `dark spot` of the panel indicates the current size compared to the original size. There is a maximum size limit of 320px in width for the thumbnails, so when the percentage goes beyond a certain point, the thumbnails will not further enlarge.

### Some details from the previous version of this document that may be worth to keep

- use left/right arrows to force moving backward/forward respectively. this works no matter it's in play/pause mode.
- click the index number, located at the top-right corner, to toggle between chronological order and random order. when it's in random order, a red border is shown around the index number whereas no border is shown when it's in chronological order. remark: since the pool size (how many images are loaded) too low (typically, one or zero) can cause problem to the code (and random order for 2 images is meaningless), i added a checking that this toggle will only work when the pool size is bigger than 2.
- you can exclude the current image from the slideshow. the control is located at the bottom-right corner. it will be shown at pause-mode. besides, since this feature will impact what has been recorded in the random order history (if any), so i took a simple solution, that is, to purge the random order history and force it back to chronological order if it was on random order when `Exclude` was clicked. but why bother adding this feature: with this feature, you may just `Choose Folder` (i.e. load all images in that folder) and exclude those images you don't want by clicking `Exclude` after everything is loaded. for some occasions, this way may be easier than using `Choose Files`. that said, the main usage probably is, using this feature to exclude a few images, as necessity arises on the spot, rather than redoing the loading process all again.
- can `drop` image(s) onto the slideshow. if the source (image) is already existing in the slideshow, the dropped image will be skipped to avoid duplication of the same image in the slideshow. this feature should work on both "drag from webpage" and "drag from file explorer". remark: for webpage, "dragging a single image" is intuitive whereas "dragging multiple images" is accomplished by dragging a text-range-selection which covered multiple images.

## Change log:

* Aug 20, 2024&nbsp;&nbsp;&nbsp;&nbsp;another bug fixed.

* Aug 18, 2024&nbsp;&nbsp;&nbsp;&nbsp;bugs fixed.

* Aug 14, 2024&nbsp;&nbsp;&nbsp;&nbsp;added the thumbnails panel (a feature for organizing the images in the slideshow).

* Jul 11, 2024&nbsp;&nbsp;&nbsp;&nbsp;added the feature to enable image(s) to `drop` onto (append to) the slideshow. and added an extra registry (the `sources.Loaded`) to avoid same source (image), caused by `drop`, from loading again if it's already existing in the slideshow.

* Jul 9, 2024&nbsp;&nbsp;&nbsp;&nbsp;added a feature to exclude the current image from the slideshow. and made some adjustments. not because there are any problems encountered, but these can make it more robust anyway.

* Jul 5, 2024&nbsp;&nbsp;&nbsp;&nbsp;cosmetic tweaks: the "loader" controls were always shown. from now on, they will be hidden in "play" mode, and shown only in "pause" mode. the "index number" control on the other hand, with some flexibility, yet still can be hidden if necessary. a rightclick on it can dismiss it. and, "pause" mode will bring all controls back (shown), including "index number".

* Jul 3, 2024&nbsp;&nbsp;&nbsp;&nbsp;added a random order feature; and bug fixes.
