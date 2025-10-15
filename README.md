# InstaFont: Multi-Language HTML Formatter README

**InstaFont** is a client-side utility designed to format text for HTML environments, specifically focusing on multi-language content within a single block of text. It automatically applies Microsoft-recommended font families based on the language script to ensure consistent and correct rendering, particularly useful for email templates that often struggle with mixed-script typography.

---
## Features

* **Language-Specific Font Mapping:** Select from a list of language groups to apply the appropriate default font family (e.g., `'Yu Gothic UI'` for Japanese, `'Nirmala UI'` for Indian Languages).
* **Font-Size Control:** Set a specific font size in points (`pt`) for the entire block.
* **Automatic Mixed-Script Handling (Japanese):** For Japanese text, the tool automatically inserts a space between Japanese characters and surrounding ASCII/Latin characters, then wraps the English/ASCII segments in a `'Segoe UI'` span to ensure proper font fallback and better kerning.
* **Right-to-Left (RTL) Support:** Automatically adds `dir="rtl"` and `text-align: right;` styling for **Arabic** text.
* **HTML Code Output:** Generates the final, production-ready HTML with inline styling.
* **Non-English Character Highlighting:** Provides a preview highlighting non-ASCII characters and offers a tooltip with the applied font and size for each character.
* **Live Preview:** Renders the generated HTML for an immediate visual check.

---
## How to Use

1.  **Set Font Size:** Enter the desired font size in the **Font size (pt)** field (default is `10.5`).
2.  **Select Language:** Choose the language group that makes up the majority of your text from the **Language group** dropdown. This will set the default font for the wrapping HTML element.
3.  **Enter Text:** Paste your plain text into the **Enter your text below** textarea.
4.  **Format:** Click the **Format Text** button to generate the output.
5.  **Review:**
    * Check the **Formatted HTML Code Output** for the generated `<div>` or `<p>` tag.
    * Review the **Non-English Characters Highlighted** area for a character-by-character breakdown and confirmation of applied fonts (hover for details).
    * Examine the final **Preview Email** area.
6.  **Copy:** Click the **Copy Code** button to copy the formatted HTML to your clipboard for use in your email or web project.

---
## Technical Details and Limitations

* **Font Hierarchy:** The outermost tag (`<p>` or `<div>`) sets the language-specific font. ASCII/Latin characters are assumed to be best rendered by `'Segoe UI'` and are explicitly wrapped where necessary (currently only for **Japanese**).
* **Line Breaks:** All newline characters (`\n`) in the input text are converted to the email-friendly HTML tag `<br />`.
* **Plain Text Only:** The application only accepts plain text input. Any existing HTML styling, images, or formatting will be lost or interpreted as plain text.
* **No External Styling:** The application only applies `font-family` and `font-size` via inline styles. It does not apply any other styling like `padding`, `margin`, or `color`.
