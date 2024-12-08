# anyfont4itch
Use any desired custom font on [itch.io](https://itch.io/) with a woff2, woff, otf, or ttf font file.

[Itch.io](https://itch.io/)'s pages are limited to the use of fonts hosted on Google Fonts. While this does allow for a multitude of options (1,731 different fonts as of 2024), many projects have custom fonts used in game or associated with their brand. Using your projects font on itch is relatively simple and will align your page with your games theming/aesthetic.

## Steps
1. [Enable CSS Account Access](https://github.com/micahmv/anyfont4itch?tab=readme-ov-file#enable-css-account-access)
2. [Convert Font File to Base64](https://github.com/micahmv/anyfont4itch?tab=readme-ov-file#convert-font-file-to-base64)
3. [Copy & Paste Custom CSS](https://github.com/micahmv/anyfont4itch?tab=readme-ov-file#copy--paste-custom-css)

## Extras
- [Helpful CSS for Text Settings & Sizing](https://github.com/micahmv/anyfont4itch?tab=readme-ov-file#helpful-css-for-text-settings--sizing)
- [Loading Font from Web](https://github.com/micahmv/anyfont4itch?tab=readme-ov-file#loading-font-from-web)
- [Examples](https://github.com/micahmv/anyfont4itch?tab=readme-ov-file#examples)

## Enable CSS Account Access
Before being able to add custom CSS for your page, you will need to enable CSS permissions for your account. This is done by sending an email to [support@itch.io](mailto:support@itch.io). 

Itch instructs to include the type of intended changes and a confirmation of only configuring visuals. See full on instructions on what to include in your email [here](https://itch.io/docs/creators/css-guide#getting-css-access). 

Response times vary, however itch generally approves all requests. Once you have your account access come back to this page and continue to the next step.

## Convert Font File to Base64
To use the font on itch.io, the file needs to be converted to Base64. This process encodes the file into a long string of characters, which can then be included with the rest of the css. To convert your file, there exist a variety of online options. I’ve used https://base64.guru/converter/encode/file for this purpose.

## Copy & Paste Custom CSS
With your account now having CSS access, paste what's below in your itch.io pages Custom CSS section from the 'Edit theme' button on your page.

Paste the relevant @font-face to the file you encoded to Base64:
```css
/* WOFF2 Web Open Font Format 2 */
@font-face {
    font-family: 'custom-font';
    src: url(data:font/woff2;charset=utf-8;base64,PASTE_BASE64_CONVERSION_OF_WOFF2_FILE_HERE) format('woff2');
}
```
```css
/* WOFF Web Open Font Format */
@font-face {
    font-family: 'custom-font';
    src: url(data:font/woff;charset=utf-8;base64,PASTE_BASE64_CONVERSION_OF_WOFF_FILE_HERE) format('woff');
}
```
```css
/* OTF OpenType */
@font-face {
    font-family: 'custom-font';
    src: url(data:font/otf;charset=utf-8;base64,PASTE_BASE64_CONVERSION_OF_OTF_FILE_HERE) format('opentype');
}
```
```css
/* TTF TrueType */
@font-face {
    font-family: 'custom-font';
    src: url(data:font/ttf;charset=utf-8;base64,PASTE_BASE64_CONVERSION_OF_TTF_FILE_HERE) format('truetype');
}
```

Paste the below to apply to a project page:
```css
/* Apply the custom font to the specified HTML elements */
/* Page content including description, more information, download, devlogs, comments, etc */
.left_col.column {
    font-family: custom-font;
}

/* Footer (bottom of the page) that shows: ITCH.IO--VIEW ALL BY CREATOR--REPORT--EMBED      TYPE*GENRE*PRICE */
.footer a {
    font-family: custom-font;
}

/* Last updated timestamp in the footer after EMBED */
.update_timestamp {
    font-family: custom-font;
}
```

Paste the below to apply to a profile page:
```css
/* Apply the custom font to the specified HTML elements */
/* Profile name */
.inner_column.text_header {
    font-family: custom-font;
}

/* Profile links */
.user_links a {
    font-family: mono;
}

/* The content of your profile page */
.user_profile.formatted {
    font-family: custom-font;
}

/* Games including their title, description, genre, and play in browser if web */
.column.game_column {
    font-family: custom-font;
}

/* Footer (bottom of the page) */
.footer {
    font-family: custom-font;
}
```

## Helpful CSS for Text Settings & Sizing

## Loading Font from Web

## Examples
