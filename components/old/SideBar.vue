<template>
  <div id="sidebar1">
    <!-- #BeginLibraryItem "/Library/Navigation.lbi" -->
    <ul id="ButterflyMenuBar" class="MenuBarVertical">
      <li>
        <a href="/">Home Page</a>
      </li>
      <li>
        <a
          href="#"
          @click="welcomeOpen = !welcomeOpen"
          :class="[ welcomeOpen ? 'MenuBarItemSubmenuHover': '', 'MenuBarItemSubmenu' ]"
        >Welcome</a>
        <ul :class="{'MenuBarSubmenuVisible': welcomeOpen}">
          <li>
            <a href="/application">Application</a>
          </li>
          <li>
            <a href="/rules">Rules and Expectations</a>
          </li>
          <li>
            <a href="/photo-gallery">Photo Gallery</a>
          </li>
        </ul>
      </li>
      <li>
        <a href="/madam">Moms &amp; Dads against Meth</a>
      </li>
      <li>
        <a href="/links">Links</a>
      </li>
      <li>
        <a
          href="#"
          @click="welcomeOpen = !welcomeOpen"
          v-bind:class="[ testimonialsOpen ? 'MenuBarItemSubmenuHover': '', 'MenuBarItemSubmenu' ]"
        >Testimonials</a>
        <ul :class="{'MenuBarSubmenuVisible': testimonialsOpen}">
          <li>
            <a href="/testimonials">Testimonials page 1</a>
          </li>
          <li>
            <a href="/testimonials2">Testimonials page 2</a>
          </li>
        </ul>
      </li>
      <li>
        <a href="/newsletter">Newsletter</a>
      </li>
      <li>
        <a href="/contact-us">Contact and Support</a>
      </li>
    </ul>
    <!-- #EndLibraryItem -->
    <h3 align="center">
      <em>A place of hope and healing</em>
    </h3>
    <p align="center">
      <a href="/newsletter">Read our Newsletters</a>
    </p>
    <p align="center" class="style4">
      <a href="https://www.facebook.com/soberliving.butterfly">
        <img src="~/static/images/facebook.png" width="64" height="64" alt>
      </a>
    </p>
    <div class="paypal">
      <form action="https://www.paypal.com/cgi-bin/webscr" method="post">
        <input type="hidden" name="cmd" value="_s-xclick">
        <input type="hidden" name="hosted_button_id" value="YGUX7UUK68NAS">
        <input
          type="image"
          src="https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif"
          border="0"
          name="submit"
          alt="PayPal - The safer, easier way to pay online!"
        >
        <img
          alt
          border="0"
          src="https://www.paypalobjects.com/en_US/i/scr/pixel.gif"
          width="1"
          height="1"
          hidden
          style="display: none !important;"
        >
      </form>
    </div>
    <p align="center" class="style3">&nbsp;</p>
    <p align="center">&nbsp;</p>
    <p align="center">
      <a href="~/static/Recipe for Monarch Butterflies.pdf">Recipe for
        <br>Monarch Butterflies
      </a>
    </p>
    <p align="center">&nbsp;</p>
    <p>
      <img
        src="~/static/images/butterfly_plant.png"
        alt="Butterfly House Butterfly on Plant"
        width="135"
        height="115"
      >
    </p>
    <p>&nbsp;</p>
    <p>&nbsp;</p>
    <p>&nbsp;</p>
    <p>&nbsp;</p>
    <p>&nbsp;</p>
  </div>
</template>

<script>
export default {
  data() {
    return { welcomeOpen: false, testimonialsOpen: false };
  }
};
</script>

<style >
@charset "UTF-8";

/* SpryMenuBarVertical.css - version 0.6 - Spry Pre-Release 1.6.1 */

/* Copyright (c) 2006. Adobe Systems Incorporated. All rights reserved. */

/*******************************************************************************

 LAYOUT INFORMATION: describes box model, positioning, z-order

 *******************************************************************************/

/* The outermost container of the Menu Bar, a fixed width box with no margin or padding */
ul.MenuBarVertical {
  margin: 0;
  padding: 0;
  list-style-type: none;
  font-size: 100%;
  cursor: default;
  width: 9em;
  /* [disabled]background-color: #477725; */
  color: #d1570d;
}
/* Set the active Menu Bar with this class, currently setting z-index to accomodate IE rendering bug: http://therealcrisp.xs4all.nl/meuk/IE-zindexbug.html */
ul.MenuBarActive {
  z-index: 1000;
  /* [disabled]background-color: #A9CC66; */
}
/* Menu item containers, position children relative to this container and are same fixed width as parent */
ul.MenuBarVertical li {
  margin: 0 0 10;
  padding: 0;
  list-style-type: none;
  font-size: 100%;
  position: relative;
  text-align: left;
  cursor: pointer;
  width: 9em;
  /* [disabled]background-color: #62B764; */
}
/* Submenus should appear slightly overlapping to the right (95%) and up (-5%) with a higher z-index, but they are initially off the left side of the screen (-1000em) */
ul.MenuBarVertical ul {
  margin: -5% 0 0 95%;
  padding: 0;
  list-style-type: none;
  font-size: 100%;
  position: absolute;
  z-index: 1020;
  cursor: default;
  width: 8.2em;
  left: -1000em;
  top: 0;
  background-color: #a9cc66;
}
/* Submenu that is showing with class designation MenuBarSubmenuVisible, we set left to 0 so it comes onto the screen */
ul.MenuBarVertical ul.MenuBarSubmenuVisible {
  left: 0;
  background-color: #a9cc66;
}
/* Menu item containers are same fixed width as parent */
ul.MenuBarVertical ul li {
  width: 8.2em;
  background-color: #a9cc66;
}

/*******************************************************************************

 DESIGN INFORMATION: describes color scheme, borders, fonts

 *******************************************************************************/

/* Outermost menu container has borders on all sides */
ul.MenuBarVertical {
  border-left-width: thin;
  border-left-color: #d1570d;
  background-color: #d4d3d2;
}
/* Submenu containers have borders on all sides */
ul.MenuBarVertical ul {
  border: 1px solid #ccc;
  background-color: #a9cc66;
}
/* Menu items are a light gray block with padding and no text decoration */
ul.MenuBarVertical a {
  display: block;
  cursor: pointer;
  padding: 0.5em 0.75em;
  color: #333;
  text-decoration: none;
  background-color: #babcb8;
  margin-bottom: 10px;
  border-radius: 20px;
  text-align: center;
}
/* Menu items that have mouse over or focus have a blue background and white text */
ul.MenuBarVertical a:hover,
ul.MenuBarVertical a:focus {
  background-color: #a9cc66;
  color: #fff;
}
/* Menu items that are open with submenus are set to MenuBarItemHover with a blue background and white text */
ul.MenuBarVertical a.MenuBarItemHover,
ul.MenuBarVertical a.MenuBarItemSubmenuHover,
ul.MenuBarVertical a.MenuBarSubmenuVisible {
  background-color: #a9cc66;
  color: #fff;
}

/*******************************************************************************

 SUBMENU INDICATION: styles if there is a submenu under a given menu item

 *******************************************************************************/

/* Menu items that have a submenu have the class designation MenuBarItemSubmenu and are set to use a background image positioned on the far left (95%) and centered vertically (50%) */
ul.MenuBarVertical a.MenuBarItemSubmenu {
  background-image: url(/images/SpryMenuBarRight.gif);
  background-repeat: no-repeat;
  background-position: 95% 50%;
  background-color: #a9cc66;
}

/* Menu items that are open with submenus have the class designation MenuBarItemSubmenuHover and are set to use a "hover" background image positioned on the far left (95%) and centered vertically (50%) */
ul.MenuBarVertical a.MenuBarItemSubmenuHover {
  background-image: url(/images/SpryMenuBarRightHover.gif);
  background-repeat: no-repeat;
  background-position: 95% 50%;
  background-color: #477725;
}

/*******************************************************************************

 BROWSER HACKS: the hacks below should not be changed unless you are an expert

 *******************************************************************************/

/* HACK FOR IE: to make sure the sub menus show above form controls, we underlay each submenu with an iframe */
ul.MenuBarVertical iframe {
  position: absolute;
  z-index: 1010;

  filter: alpha(opacity: 0.1);
  background-color: #477725;
}
/* HACK FOR IE: to stabilize appearance of menu items; the slash in float is to keep IE 5.0 from parsing */
@media screen, projection {
  ul.MenuBarVertical li.MenuBarItemIE {
    display: inline;
    float: left;
    background-color: #477725;
  }
}
</style>