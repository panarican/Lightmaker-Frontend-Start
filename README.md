Lightmaker-Frontend-Start
=========================

<h2>Have a folder structured like:</h2>
    assets
js (no javascript will be in base except for main.js)
main.js  (require in all initial modules)
modules (compressed files go here)
modules-uncompressed (uncompressed files go here)
(namespace folders)
vendor (plugin, things we did not create)
require.js (always needed)
html5shiv.js (for compatibility with IE8)
css
sass
styles.scss
images (no imagery in base folder)
global (all layout-based imagery. header/footer)
(namespace folders)
What should the main.js file look like:

(example main.js file included)

Define goes at the top
List all dependencies
Javascript module configuration:

(example javascript module)

All globally shared variables will be defined in the config method.
Classes will all be capitalized (ex. Class)
Methods inside of the class will be camel case (ex. camelCase)
Variable naming:
Underscored variables will be private to the method it is incapsulated (ex. _self)
Referencing jQuery objects, use $ in front of the name (ex. $content)
Variables that are defined within the config method will be camel case.
Constants will be all caps (ex. CONSTANT)
Don't abbreviate variables (For legibility sake, ex. _index instead of i)
Init method
All methods that need to be called on page load
Events method
All methods that are events (ex. On events)
(Namespacing methods)
No javascript file should be longer than 800 lines of code
re-evaluate if longer
Comment every method, explain how it works and what it is trying to do
CSS
(Create sample SCSS folder)
Use COMPASS do not use vendor prefixes (ex. no -webkit-, or -moz-).
No sass file will be styling a "page" only "modules"
Class names will be lowercase and dash separated (ex. .module-name)
Class names will be named after the piece they are styling, not descriptive of their styles (do NOT use .colorGrey or .style1)
Media queries will live within the immediate module class, not within the individual classes inside it.
Always tab space and put properties on their own lines.
Try not to ever duplicate CSS, if written correctly, you should be able to take any class and just plug it in.
Do NOT go deeper than 4 classes deep.
Never style IDs.
Style ONLY classes except for html, body, and a tags.
The only other time to style elements is inside a WYSIWYG content area.
All icons will be using Icomoon.
Move the SVG link below EOT in the Fonts properties. (It looks smoother in Windows)
All fonts will be specified inside the _fonts.scss
All icons will be specified inside the _icons.scss
All global variables need to be specified inside the _vars.scss
Every element will be defined the following:
@include box-sizing(border-box);
Comment all "modules, all sections within those "modules", and variations of those "modules"

Pushing to Live:
Minify all CSS and Javascript before pushing to Live