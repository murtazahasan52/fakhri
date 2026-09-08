BRAND LOGOS — how to swap the text wordmarks for real logos
===========================================================

The "Brands on our shelves" strip scrolls on its own. Right now each brand shows
as a styled wordmark (plain text), because no logo image files ship with the site.

TO USE A REAL LOGO
------------------
1. Put the logo file in this folder, e.g.  images/brands/dulux.png
   - PNG with a transparent background, or SVG
   - roughly 300-500 px wide, height whatever the logo needs
   - the strip renders them at 38 px tall, greyscale, and colours them on hover

2. In index.html, find the brand strip (search for `id="brandset"`) and replace
   that one item's span with an img:

   BEFORE
     <div class="mq-item"><span class="mq-word">Dulux<small>AkzoNobel</small></span></div>

   AFTER
     <div class="mq-item"><img src="images/brands/dulux.png" alt="Dulux" /></div>

   Do this for as many as you have files for — text and logos can sit side by side.

TO ADD OR REMOVE A BRAND
------------------------
Add or delete a whole `<div class="mq-item">…</div>` line inside `#brandset`.
The second copy of the strip is cloned by JavaScript at load, so you only ever
edit the one list. Around 8-14 items keeps the scroll looking full.

SPEED
-----
`animation: mqscroll 38s linear infinite` in the CSS — raise the seconds to slow
it down, lower to speed it up. It pauses while the cursor is over the strip, and
stops entirely for visitors who have "reduce motion" switched on.

WHICH BRANDS ARE LISTED
-----------------------
Confirmed from your own photos and catalogue:
  Dulux (AkzoNobel), Kansai Nerolac, Nerolac Excel, Starlite,
  Araldite, Bondtite, Bull Bond

Added as common stock for a shop like yours — DELETE ANY YOU DON'T ACTUALLY CARRY:
  Fevicol, Astral, Supreme, Finolex, Birla White

A NOTE ON USING BRAND LOGOS
---------------------------
Logos are the trademarks of their owners. Dealers normally display the logos of
brands they genuinely stock, and most companies supply dealer artwork on request
(ask your Dulux / Nerolac distributor). Only list brands you actually sell.
