
| Command                | Description                                                                        |
| ---------------------- | ---------------------------------------------------------------------------------- |
| mceRetrieveFormats     | Retrieves the formats from the current selection.                                  |
| mcePaintFormats        | Applies the formats retrieved using `mceRetrieveFormats` to the current selection. |
| mceToggleFormatPainter | Toggles the Format Painter.                                                        |

**Examples**

```js
tinymce.activeEditor.execCommand('mceRetrieveFormats');
tinymce.activeEditor.execCommand('mcePaintFormats');
tinymce.activeEditor.execCommand('mceToggleFormatPainter');
```