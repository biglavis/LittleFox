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

## Features

LittleFox is designed to be mouse friendly while maintaining a minimalist aesthetic. This theme draws inspiration from [Cascade](https://github.com/cascadefox/cascade), adapting several of its design elements with tweaks to improve mouse usability, while also introducing many original features such as:

**Dynamic UI Buttons**

![DynamicButtons](/assets/DynamicButtons.gif)

**Customizable Floating Find Bar**

![Findbar](/assets/Findbar.gif)

**... and more!**

## Customization

Several UI elements can be customized by changing the variable values at the top of [**`userChrome.css`**](https://github.com/biglavis/LittleFox/blob/main/userChrome.css).

```css
/*  ,-----. ,-----. ,--.  ,--.,------.,--. ,----.    
 * '  .--./'  .-.  '|  ,'.|  ||  .---'|  |'  .-./    
 * |  |    |  | |  ||  |' '  ||  `--, |  ||  | .---. 
 * '  '--'\'  '-'  '|  | `   ||  |`   |  |'  '--'  | 
 *  `-----' `-----' `--'  `--'`--'    `--' `------'  
 */

:root {
  /* Navigation Bar Width
   * Max width is applied when url bar is expanded.
   */
  --navbar-width: max(35vw, 500px);
  --navbar-max-width: max(60vw, 800px);

  /* Dynamic Tab Width */
  --active-tab-width: clamp(100px, 24vw, 240px);    
  --inactive-tab-width: clamp(100px, 18vw, 180px);

  /* Dynamic Bookmarks Toolbar
   * If enabled, hide bookmarks toolbar and show when url bar is hovered
   * Ensure bookmarks toolbar is set to "always show" for proper behavior
   * Enabled: 1, absolute
   * Disabled: 0, static
   */
  --dynamic-bookmarks: 1; --bookmarks-position: absolute;
  /* --dynamic-bookmarks: 0; --bookmarks-position: static; */

  /* Dynamic Bookmarks Toolbar Hover Delay */
  --dynamic-bookmarks-hover-delay: 450ms;

  /* Dynamic Bookmarks Toolbar Hide Delay */
  --dynamic-bookmarks-hide-delay: 50ms;

  /* Preferred Find Bar Width
   * Set to 0px for minimum width
   */
  --findbar-width: calc(var(--findbar-min-width-expanded) + (100vw - 2 * var(--findbar-right) - var(--findbar-min-width-expanded)) * 0.12);

  /* Find Bar Distance from Window Corners */
  --findbar-top: 12px;
  --findbar-right: max(2vw, 24px); /* scrollbar is 12px */

  /* Show/Hide Find Bar Options
   * Show: 1
   * Hide: 0
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
