Lightmaker-Frontend-Start
=========================

<h2>Have a folder structured like:</h2>

<ul>
	<li>assets
		<ul>
			<li>js (no javascript will be in base except for main.js)
				<ul>
					<li>main.js  (require in all initial modules)</li>
					<li>modules (compressed files go here)</li>
					<li>modules-uncompressed (uncompressed files go here)
						<ul>
							<li>(namespace folders)</li>
						</ul>
					</li>
					<li>vendor (plugin, things we did not create)
						<ul>
							<li>require.js (always needed)</li>
							<li>html5.js (for compatibility with IE8)</li>
						</ul>
					</li>
				</ul>
			</li>
			<li>css</li>
			<li>sass
				<ul>
					<li>styles.scss</li>
				</ul>
			</li>
			<li>fonts (all webfonts need to be in here)</li>
			<li>icons (all Icomoon fonts need be in here)</li>
			<li>images (no imagery in base folder)
				<ul>
					<li>global (all layout-based imagery. header/footer)</li>
				</ul>
			</li>
			<li>(namespace folders)</li>
		</ul>
	</li>
</ul>

<h2>What should the main.js file look like:</h2>
(example main.js file included)
<ul>
	<li>Define goes at the top
		<ul>
			<li>List all dependencies</li>
		</ul>
	</li>
</ul>

<h3>Javascript module configuration:</h3>
(example javascript module)
<ul>
	<li>All globally shared variables will be defined in the config method.</li>
	<li>Classes will all be capitalized (ex. Class)</li>
	<li>Methods inside of the class will be camel case (ex. camelCase)</li>
	<li>Variable naming:
		<ul>
			<li>Underscored variables will be private to the method it is incapsulated (ex. _self)</li>
			<li>Referencing jQuery objects, use $ in front of the name (ex. $content)</li>
			<li>Variables that are defined within the config method will be camel case.</li>
			<li>Constants will be all caps (ex. CONSTANT)</li>
			<li>Don't abbreviate variables (For legibility sake, ex. _index instead of i)</li>
		</ul>
	</li>
	<li>Init method
		<ul>
			<li>All methods that need to be called on page load</li>
		</ul>
	</li>
	<li>Events method
		<ul>
			<li>All methods that are events (ex. On events)</li>
		</ul>
	</li>
	<li>(Namespacing methods)</li>
	<li>No javascript file should be longer than 800 lines of code
		<ul>
			<li>re-evaluate if longer</li>
		</ul>
	</li>
	<li>Comment every method, explain how it works and what it is trying to do</li>
</ul>

<h2>CSS</h2>
(Create sample SCSS folder)
<ul>
	<li>Use COMPASS do not use vendor prefixes (ex. no -webkit-, or -moz-).</li>
	<li>No sass file will be styling a "page" only "modules"</li>
	<li>Class names will be lowercase and dash separated (ex. .module-name)</li>
	<li>Class names will be named after the piece they are styling, not descriptive of their styles (do NOT use .colorGrey or .style1)</li>
	<li>Media queries will live within the immediate module class, not within the individual classes inside it.</li>
	<li>Always tab space and put properties on their own lines.</li>
	<li>Try not to ever duplicate CSS, if written correctly, you should be able to take any class and just plug it in.</li>
	<li>Do NOT go deeper than 4 classes deep.</li>
	<li>Never style IDs.</li>
	<li>Style ONLY classes except for html, body, and a tags.
		<ul>
			<li>The only other time to style elements is inside a WYSIWYG content area.</li>
		</ul>
	</li>
	<li>All icons will be using Icomoon.</li>
	<li>Move the SVG link below EOT in the Fonts properties. (It looks smoother in Windows)</li>
	<li>All fonts will be specified inside the _fonts.scss</li>
	<li>All icons will be specified inside the _icons.scss</li>
	<li>All global variables need to be specified inside the _vars.scss</li>
	<li>Every element will be defined the following:
		<ul>
			<li>@include box-sizing(border-box);</li>
		</ul>
	</li>
	<li>Comment all "modules, all sections within those "modules", and variations of those "modules"</li>
</ul>

<h2>Pushing to Live:</h2>
<ul>
	<li>Minify all CSS and Javascript before pushing to Live</li>
</ul>