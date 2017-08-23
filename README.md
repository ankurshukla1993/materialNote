# MaterialNote v2

WYSIWYG editor for the web, based on materialnote.js and materializeCss.

MaterialNote v2 is a work-in-progress for better sync with orignal materialnote repo;
MaterialNote v1.2.1 is currently the latest release.


## Editor Api

MaterialNote is based on materialnote.js, so the API is still the same.
Please visit [materialnote.js api guide](http://materialnote.org/deep-dive/) to deep dive.


## Improvements

Other than the obvious changes to the UI to meet material style, there are some differences and improvements in materialNote;

- edited image popover to be shown always in the editor area
- fided scroll causing linkPopover to be shown outside editor's area
- options have been added to image and table dropdowns to handle materialize's styles for those items
- color palette dropdown has been edited to meet materialize's color palette


## API additions


## Settings additions

Other to the standard summernote.js settings, materialNote have some extras (take a look at official summernote guide for the [summernote.js initialization options](http://summernote.org/deep-dive/#initialization-options)).

- `popover.image`: added `['responsivity', ['responsive']]` btn group containing button to handle materialize's image responsivity class.
- `popover.link`: added `openLinkNewWindow` btn to handle `target` attribute of the link directly from the popover.
- `popover.table`: added `['materializeOptions', ['borderedTable', 'stripedTable', 'highlightedTable', 'responsiveTable', 'centeredTable']]` btn group to handle materialize's table options.
- `defaultColors.text`: default text color used for recent-color button at startup.
- `defaultColors.background`: default background color used for recent-color button at startup.


## Editor colors

If you wish to change any of the editor color, you can quickly achieve the desired result by editing file **src/less/variables.scss**, which defines all colours used by the editor as sass variables.

After making desired changes, just run `grunt build` to create a new dist in the **dist** folder.
