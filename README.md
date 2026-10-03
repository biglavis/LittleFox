<div align="center">

# LittleFox

**A minimalistic, mouse centered CSS theme for FireFox, inspired by [Cascade](https://github.com/cascadefox/cascade).**

![Preview](/assets/head.webp)

</div>

## Installation

1. Download [**`userChrome.css`**](https://github.com/biglavis/LittleFox/blob/main/userChrome.css).

2. Go to **`about:config`** in FireFox. Search for **`toolkit.legacyUserProfileCustomizations.stylesheets`** and set it to **`true`**.

3. Go to **`about:support`** in FireFox and open your Profile Folder. Create a new folder named **`chrome`** if it does not already exist.

4. Copy the downloaded [**`userChrome.css`**](https://github.com/biglavis/LittleFox/blob/main/userChrome.css) into the **`chrome`** folder and restart Firefox.

## Key Features

**Dynamic UI Buttons**

![DynamicButtons](/assets/dynamic_buttons.webp)

**Dynamic Bookmarks Toolbar**

![DynamicBookmarks](/assets/dynamic_bookmarks_toolbar.webp)

**Customizable Floating Find Bar**

![Findbar](/assets/findbar.webp)

## Customization

Several UI elements can be customized by modifying the variable values at the top of [**`userChrome.css`**](https://github.com/biglavis/LittleFox/blob/main/userChrome.css).

```css
/*  ,-----. ,-----. ,--.  ,--.,------.,--. ,----.    
 * '  .--./'  .-.  '|  ,'.|  ||  .---'|  |'  .-./    
 * |  |    |  | |  ||  |' '  ||  `--, |  ||  | .---. 
 * '  '--'\'  '-'  '|  | `   ||  |`   |  |'  '--'  | 
 *  `-----' `-----' `--'  `--'`--'    `--' `------'  
 */

:root {
  /* Navigation Bar Width*/
  --navbar-width: max(35vw, 500px);

  /* URL Bar Open Width
   * Applied when the URL bar is open.
   * Set to auto to keep width unchanged.
   */
  --urlbar-open-width: max(60vw, 800px);

  /* Dynamic Tab Width */
  --active-tab-width: clamp(100px, 24vw, 240px);    
  --inactive-tab-width: clamp(100px, 18vw, 180px);

  /* Dynamic Toolbar Buttons Hover Delay
   * Hover hamburger menu to reveal additional toolbar buttons.
   */
  --dynamic-buttons-hover-delay: 450ms;

  /* Dynamic Bookmarks Toolbar
   * If enabled, hide bookmarks toolbar and show when url bar is hovered.
   * Ensure bookmarks toolbar is set to "always show" for proper behavior.
   * 0: Disabled
   * 1: Enabled
   */
  --dynamic-bookmarks: 1;

  /* Dynamic Bookmarks Toolbar Hover Delay */
  --dynamic-bookmarks-hover-delay: 450ms;

  /* Dynamic Bookmarks Toolbar Hide Delay */
  --dynamic-bookmarks-hide-delay: 50ms;

  /* Floating Bookmarks Toolbar
   * (Only with dynamic bookmarks toolbar enabled)
   * 0: Disabled
   * 1: Enabled
   */
  --floating-bookmarks: 1;

  /* Floating Bookmarks Toolbar Width Mode
   * Controls how the floating bookmarks toolbar sizes itself in one-line layout.
   * 0 : Dynamic - Minimum width aligns with the navigation bar.
   * 1 : Compact - Shrinks to wrap tightly around bookmarks.
   * 2 : Full    - Spans from the left edge to the right edge of the window.
   */
   --floating-bookmarks-width-mode: 0;

  /* Floating Bookmars Toolbar Distance from Window Corners */
  --floating-bookmarks-top: 6px;
  --floating-bookmarks-inline: 8px;

  /* Find Bar Width
   * Set to 0px for minimum width.
   * Set to 100vw for maximum width.
   */
  --findbar-width: calc(var(--findbar-min-width) + (100vw - 2 * var(--findbar-right) - var(--findbar-min-width)) * 0.12);

  /* Find Bar Distance from Window Corners */
  --findbar-top: 12px;
  --findbar-right: max(2cqw, 16px);

  /* Show/Hide Find Bar Options
   * 0: Hide
   * 1: Show
   */
  --show-highlight-all:    1;
  --show-match-case:       1;
  --show-match-diacritics: 1;
  --show-whole-words:      1;

  /* Find Bar Options Position */
  --highlight-all-position:    0;
  --match-case-position:       1;
  --match-diacritics-position: 2;
  --whole-words-position:      3;
}
```

## Acknowledgements

* Inspired by and adapted from **[Cascade](https://github.com/cascadefox/cascade)**.
* Shoutout to **[FoxOne](https://github.com/Firnschnee/FoxOne)** for the `@container` logic used in the dynamic bookmarks toolbar.
