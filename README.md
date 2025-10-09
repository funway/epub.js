# hawu-epubjs
This is my personal fork of epub.js with some fixes. 

Based on [epub.js v0.3.93](https://www.npmjs.com/package/epubjs/v/0.3.93).

## Changes include
- Fix potential memory leaks
  - Replaced anonymous unload event listener in `DefaultViewManager` and `ContinuousViewManager` with a named function, ensuring proper cleanup.
  - Updated their `removeEventListeners` to correctly remove unload handlers.
  - Fixed a typo in `Stage.destroy()` where "`orientationchange`" was misspelled.
