CodeMirror Composition Mod for 5.x
==========================

When you use IMEs to composite non-latin charaters like Chinese or Japanese, you'll notice that you cannot see the composition text decorated well (usually _underlined_). You cannot see your cursor moving during compositing either, because the cursor of CodeMirror is a `<div>` rather than a real cursor.

This add-on tries to enhance the composition experience of CodeMirror for IME users with the [Composition Event][2] APIs.

## Usage

```
npm install codemirror-composition-mod --save-dev
```

link `lib/codemirror-composition-mod.css`

```html
<link rel="stylesheet" type="text/css" href="lib/codemirror-composition-mod.css" />
```

```coffee
require('codemirror-composition-mod')(CodeMirror)
CodeMirror.fromTextArea(el, {
  enableCompositionMod: true
});
```

## Modification to CodeMirror instance

This mod adds 5 additional properties to the CodeMirror instance:

```js
cm.display.inCompositionMode //(Boolean)
cm.display.compositionHead //(Pos)
cm.display.textMarkerInComposition //(TextMarker)
```
