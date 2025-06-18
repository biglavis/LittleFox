<div align="center">

# LittleFox

**A minimalistic, mouse centered CSS theme for FireFox, inspired by [Cascade](https://github.com/cascadefox/cascade).**

![Preview](/images/LittleFox.png)

</div>

## Installation

1. Download [**`userChrome.css`**](https://github.com/biglavis/LittleFox/blob/main/userChrome.css).

2. Go to **`about:config`** in FireFox. Search for **`toolkit.legacyUserProfileCustomizations.stylesheets`** and set it to **`true`**.

3. Go to **`about:support`** in FireFox and open your Profile Folder. Create a new folder named **`chrome`** if it does not already exist.

4. Copy the downloaded [**`userChrome.css`**](https://github.com/biglavis/LittleFox/blob/main/userChrome.css) into the **`chrome`** folder and restart Firefox.

## Features

LittleFox is designed to be mouse friendly while maintaining a minimalist aesthetic. This theme draws inspiration from [Cascade](https://github.com/cascadefox/cascade), adapting several of its design ideas alongside many original features such as:

**Dynamic UI Buttons**

![DynamicButtons](/images/DynamicButtons.gif)

**A Highly Customizable, Floating Findbar**

![Findbar](/images/Findbar.gif)

**... and more!**

## Customization

Several UI elements can be customized by changing the variable values at the top of **`userChrome.css`**.

```css
/*  ,-----. ,-----. ,--.  ,--.,------.,--. ,----.    
 * '  .--./'  .-.  '|  ,'.|  ||  .---'|  |'  .-./    
 * |  |    |  | |  ||  |' '  ||  `--, |  ||  | .---. 
 * '  '--'\'  '-'  '|  | `   ||  |`   |  |'  '--'  | 
 *  `-----' `-----' `--'  `--'`--'    `--' `------'  
 */

:root {
  /* Show/hide reload button
   * show: flex
   * hide: none
   */
  --show-reload: none;

  /* Navigation toolbar width
   * max width is applied when url bar is expanded
   */
  --navbar-width: max(35vw, 500px);
  --navbar-max-width: max(60vw, 800px);

  /* Dynamic tab width */
  --active-tab-width: clamp(100px, 24vw, 240px);    
  --inactive-tab-width: clamp(100px, 18vw, 180px);

  /* Preferred find bar width
   * set to 0px for minimum width
   */
  --findbar-width: calc(var(--findbar-min-width-expanded) + (100vw - var(--findbar-min-width-expanded)) * 0.1);

  /* Find bar distance from window corners */
  --findbar-top: 12px;
  --findbar-right: max(2vw, 30px); /* scrollbar is 18px */

  /* Find bar transition duration */
  --findbar-transition-duration: 100ms;

  /* Find bar transition length */
  --findbar-transition-length: 20px;

  /* Show/hide find bar options
   * show: 1
   * hide: 0
   */
  --show-highlight-all:    1;
  --show-match-case:       1;
  --show-match-diacritics: 1;
  --show-whole-words:      1;

  /* Find bar options position */
  --highlight-all-position:    0;
  --match-case-position:       1;
  --match-diacritics-position: 2;
  --whole-words-position:      3;
}
```
