# anyfont4itch
Use any desired custom font on [itch.io](https://itch.io/) with a woff2, woff, otf, or ttf font file.

[Itch.io](https://itch.io/)'s pages are limited to the use of fonts hosted on Google Fonts. While this does allow for a multitude of options (1,731 different fonts as of 2024), many projects have custom fonts used in game or associated with their brand. Using your projects font on itch is relatively simple and will align your page with your games theming/aesthetic.

## Steps
- [CSS Account Access](https://github.com/micahmv/anyfont4itch?tab=readme-ov-file#css-account-access)
- [Convert Font File to Base64](https://github.com/micahmv/anyfont4itch?tab=readme-ov-file#convert-font-file-to-base64)
- [Copy & Paste](https://github.com/micahmv/anyfont4itch?tab=readme-ov-file#copy--paste)

## CSS Account Access
Before being able to add custom CSS for your page, you will need to enable CSS permissions for your account. This is done by sending an email to [support@itch.io](mailto:support@itch.io). 

Itch instructs to include the type of intended changes and a confirmation of only configuring visuals. See full on instructions on what to include in your email [here](https://itch.io/docs/creators/css-guide#getting-css-access). 

Response times vary, however itch generally approves all requests. Once you have your account access come back to this page and continue to the next step.

## Convert Font File to Base64
To use the font on itch.io, the file needs to be converted to Base64. This process encodes the file into a long string of characters, which can then be included with the rest of the css. To convert your file, there exist a variety of online options. I’ve used https://base64.guru/converter/encode/file for this purpose.

## Copy & Paste
Use the relevant @font-face to the file you encoded to Base64.
```css
/* WOFF2 */
@font-face {
    font-family: 'custom-font';
    src: url(data:font/woff2;charset=utf-8;base64,PASTE_BASE64_CONVERSION_OF_WOFF2_FILE_HERE) format('woff2');
}
```
```css
```
/* WOFF2 */
@font-face {
    font-family: 'custom-font';
         url(data:font/woff;charset=utf-8;base64,PASTE_BASE64_CONVERSION_OF_WOFF_FILE_HERE) format('woff');
}
```
         url(data:font/woff;charset=utf-8;base64,PASTE_BASE64_CONVERSION_OF_WOFF_FILE_HERE) format('woff'),      /* Older browsers */
         url(data:font/otf;charset=utf-8;base64,PASTE_BASE64_CONVERSION_OF_OTF_FILE_HERE) format('opentype'),   /* OTF OpenType format */
         url(data:font/ttf;charset=utf-8;base64,PASTE_BASE64_CONVERSION_OF_TTF_FILE_HERE) format('truetype');   /* TTF TrueType for very old browsers */
}
```
