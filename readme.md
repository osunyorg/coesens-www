# Coesens website

## About Osuny

[Documentation officielle sur developers.osuny.org](https://developers.osuny.org/docs/website/)

## Architecture

Styling files all located in **assets > sass directory** :
* blocks
  * _areas-of-expertise.sass
  * _homepage.sass
* _configuration.sass
* _design-system.sass
* _fonts.sass
* main.sass

**4 partials in layouts directory** : one for the footer, three for section hero pages (projects, posts, persons)

## Design system

### Global

Special styling in **_design-system.sass** :
* **Hero** : image sizing and positioning (contain, top-aligned) on section pages with image
* **Hero** : white background on persons, posts, projects single pages and contact page
* **Hero** : portrait/square images — bottom margin removed on mobile
* **External links** : arrow icon after external links removed globally
* **Email icon** : custom remixicon email icon in footer
* **Body** : full-height flex layout to stick footer at bottom of page

## Blocks

### Homepage

Special styling in **_homepage.sass** and **_design-system.sass**.

Custom html selectors added through Osuny's backoffice include :
* `block-class-grid-areas-of-expertise` : for gallery block : 6 images per row on desktop, images at 80% width
* `block-class-homepage-projects-block` : for projects block : alternate background color, card layout with image cover and "more" link pinned to bottom
* `block-class-posts-list-block` : for posts block : rounded corners on post images
* `block-class-homepage-cta-block` : for CTA block : custom button styling with external link icon

Special styling in **_design-system.sass** :
* **Homepage button** : custom button style (accent background, border-radius, arrow icon, hover state)

### Areas of expertise page

Special styling in **_areas-of-expertise.sass**.

Custom html selectors added through Osuny's backoffice include :
* `block-class-categories-areas-of-expertise` : for categories block : 3 columns on desktop, image unset aspect ratio at 50% width, h3 title
* `block-class-gallery-area-of-expertise` : for gallery block : 4 images per row on desktop, square images with contain fit
* `block-class-links-area-of-expertise` : for links block : 3 columns on desktop, images with cover + top positioning

### Projects list page

Special styling in **_design-system.sass** :
* Projects grid : 3 columns on desktop, 16/9 images with contain fit, "more" link hidden, arrow icon on project title with hover animation
* Mobile : project images stay within container (no bleed)

### Projects by category pages

Same layout as the projects list page, with an additional hero image size override on desktop (336×336px).

### Posts list page

Special styling in **_design-system.sass** :
* Post images : full-width on mobile (overrides default 33% thumbnail), 3/2 aspect ratio, cover fit, rounded corners (asymmetric border-radius)
* Image size config overridden in `config/_default/config.yaml` : `posts.layouts.list.mobile` set to 400px to avoid pixelation at full width

## Partials

### Section hero subtitles

Three local overrides to display subtitles in section page heroes (not included by default in the theme) :
* layouts > partials > projects > section : hero.html
* layouts > partials > posts > section : hero.html
* layouts > partials > persons > section : hero.html

### Footer

* **Partial** to display Coesens' postal address (131 rue de Créqui, 69006 Lyon) at the same level as the logo. Partial is located in layouts > partials > footer : site.html