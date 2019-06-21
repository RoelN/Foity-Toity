# Foity Toity

**WORK IN PROGRESS! The following instructions are not correct!**

⚠️ The reason why this doesn't work is described [in this issue](https://github.com/RoelN/Foity-Toity/issues/1).

Foity Toity is a font that makes all text disappear. It contain an empty, zero width glyph for every Unicode code point.

Foity Toity is based on [Adobe Blank 2](https://github.com/adobe-fonts/adobe-blank-2) with some optimisations applied (it's about one third the size of Adobe Blank 2).

## Why?

Text on a website will be shown in a fallback font until your web font has finished loaded. This is the [FOUT](https://www.zachleat.com/web/webfont-glossary/#fout) and is usually desirable: your visitors can start reading the text right away. But there are situations where you might want to keep the text invisible until your web font has loaded: the [FOIT](https://www.zachleat.com/web/webfont-glossary/#foit).

For example when using icon fonts, to make sure you definitely don't see anything until the icon font has loaded. Or font specimens, portfolios or design-heavy sites where you deliberately want to wait till your web font has loaded.

## How to use

Foity Toity is a super tiny CSS snippet (690 bytes) that inlines a font that makes all text invisible. Put the `hoity-toity.css` snippet it in your `<head>` so it's immediately available. Then use it after your desired font in the font stack, like so:

```
h1 {
    font-family: MyDesiredFont, foity-toity;
}
```

Foity Toity uses a WOFF2 font, so [some older browsers](https://caniuse.com/#feat=woff2) aren't supported. If you want this to work in IE11 and similar vintage web surfing software, use `foity-toity-legacy.css` which uses an OTF font. If you need the font binaries, check the `fonts` directory.

## Questions?

Open an issue or ping me on [@pixelambacht](https://twitter.com/pixelambacht)!
