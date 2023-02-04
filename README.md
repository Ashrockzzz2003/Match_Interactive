# Interactive Matching Game - Gods and Vahanas

"Match the gods with their ride, test your divine knowledge with our interactive game."

## Table of Contents

1. Overview
2. How to Play
3. Code


## Overview

This game presents the player with a set of gods on one side and vahanas on the other. The player must match each god with their correct vahana. The game ends when all gods have been matched with their respective vahanas.

## How to Play

- On the left side of the screen, the player will see a list of gods.
- On the right side of the screen, the player will see a list of vahanas.
- The player must click and drag each god to its correct vahana.
- If the player matches a god with the correct vahana, the game will indicate a correct match `green`.
- If the player matches a god with an incorrect vahana, the game will indicate an incorrect match `red`.
- The game ends when all gods have been matched with their respective vahanas.

## Frameworks Used

The game is made with `HTML`, `CSS`, and `JavaScript`. 

## File Structure

- **ganesha.png**: image of Ganesha
- **murugan.png**: image of Murugan
- **shiva.png**: image of Shiva
- **vishnu.png**: image of Vishnu
- **durga.png**: image of Durga
- **ganesha_1.png**: image of Ganesha's vahana
- **murugan_1.png**: image of Murugan's vahana
- **shiva_1.png**: image of Shiva's vahana
- **vishnu_1.png**: image of Vishnu's vahana
- **durga_1.png**: image of Durga's vahana


## HTML Structure

<p>The game is contained within a <code>div</code> with class <code>game-container</code>. It contains two sections - <code>left</code> and <code>right</code>, with the class <code>match-items</code> and <code>match-targets</code> respectively. Each section contains <code>div</code>s with class <code>match-item</code> and <code>match-target</code>, respectively, for the gods and their vahanas.</p>

The `data-match` attribute is used to specify the match between the gods and their vahanas.

## CSS Styling

<ul><li>The font used for the game is "Poppins" from Google Fonts.</li><li>The <code>game-container</code> <code>div</code> has display set to <code>flex</code>, with <code>justify-content</code> set to <code>center</code> and with a <code>border</code>, <code>border-radius</code> and <code>box-shadow</code>.</li><li>The <code>match-item</code> and <code>match-target</code> classes have a <code>width</code> set to <code>fit-content</code>, with <code>margin</code> and <code>padding</code> specified.</li><li>The <code>match-item</code> and <code>match-target</code> classes have a <code>cursor</code> set to <code>move</code>.</li><li>On hover, the <code>border-radius</code> of the <code>match-item</code> and <code>match-target</code> changes to <code>16px</code>.</li><li>The <code>on_swap</code> class changes the background and <code>border-radius</code> of the element, and also adds a <code>box-shadow</code>.</li></ul>

## JavaScript Functionality

The following JavaScript code implements a matching game with two sections: 
- the left section and the right section. 
- The `Sortable.js` library is used to allow the items in each section to be reordered.

### randomize(id) function
This function takes an `id` parameter which is a selector for either the left or right section. It randomly rearranges the items within that section.

### validate() function
This function checks if the items in the left section are correctly matched with the items in the right section. If they are, it displays a "Congratulations" message. If they are not, the incorrect items are highlighted with a red border.

### launch_toast(message) function
This function displays a message using a toast notification.

### Sortable.create() method
Two Sortable instances are created using the `Sortable.create()` method: one for the left section and one for the right section. The options for each instance specify animation and ease of movement, define the group for each section so that items can only be reordered within their own section, and specify a swap class and callback function `onEnd` to be executed after an item is reordered.
