<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>InstaFont README</title>
    <style>
        body {
            font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
            max-width: 800px;
            margin: 40px auto;
            padding: 20px 30px;
            background: #ffffff;
            color: #333;
            line-height: 1.6;
            border: 1px solid #ddd;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
        }
        h1, h2, h3 {
            color: #34495e;
        }
        h1 {
            font-size: 2.2rem;
            text-align: center;
            border-bottom: 2px solid #3498db;
            padding-bottom: 10px;
            margin-bottom: 30px;
        }
        h2 {
            font-size: 1.6rem;
            margin-top: 30px;
            border-left: 5px solid #3498db;
            padding-left: 10px;
        }
        p {
            margin-bottom: 15px;
        }
        .highlight {
            background-color: #ecf0f1;
            padding: 2px 5px;
            border-radius: 4px;
            font-family: 'Courier New', Courier, monospace;
        }
        ul {
            list-style-type: disc;
            margin-left: 20px;
            margin-bottom: 20px;
        }
        li {
            margin-bottom: 8px;
        }
        code {
            font-family: 'Courier New', Courier, monospace;
            background-color: #f5f5f5;
            padding: 1px 4px;
            border-radius: 3px;
            color: #c0392b;
        }
    </style>
</head>
<body>

    <h1>InstaFont: Multi-Language HTML Formatter</h1>

    <p><strong>InstaFont</strong> is a client-side utility designed to format text for HTML environments, specifically focusing on multi-language content within a single block of text. It automatically applies Microsoft-recommended font families based on the language script to ensure consistent and correct rendering, particularly useful for email templates that often struggle with mixed-script typography.</p>

    <h2>Features</h2>
    <ul>
        <li><strong>Language-Specific Font Mapping:</strong> Select from a list of language groups to apply the appropriate default font family (e.g., <span class="highlight">'Yu Gothic UI'</span> for Japanese, <span class="highlight">'Nirmala UI'</span> for Indian Languages).</li>
        <li><strong>Font-Size Control:</strong> Set a specific font size in points (<span class="highlight">pt</span>) for the entire block.</li>
        <li><strong>Automatic Mixed-Script Handling (Japanese):</strong> For Japanese text, the tool automatically inserts a space between Japanese characters and surrounding ASCII/Latin characters, then wraps the English/ASCII segments in a <span class="highlight">'Segoe UI'</span> span to ensure proper font fallback and better kerning.</li>
        <li><strong>Right-to-Left (RTL) Support:</strong> Automatically adds <span class="highlight">dir="rtl"</span> and <span class="highlight">text-align: right;</span> styling for **Arabic** text.</li>
        <li><strong>HTML Code Output:</strong> Generates the final, production-ready HTML with inline styling.</li>
        <li><strong>Non-English Character Highlighting:</strong> Provides a preview highlighting non-ASCII characters and offers a tooltip with the applied font and size for each character.</li>
        <li><strong>Live Preview:</strong> Renders the generated HTML for an immediate visual check.</li>
    </ul>

    <h2>How to Use</h2>
    <ol>
        <li><strong>Set Font Size:</strong> Enter the desired font size in the **Font size (pt)** field (default is <span class="highlight">10.5</span>).</li>
        <li><strong>Select Language:</strong> Choose the language group that makes up the majority of your text from the **Language group** dropdown. This will set the default font for the wrapping HTML element.</li>
        <li><strong>Enter Text:</strong> Paste your plain text into the **Enter your text below** textarea.</li>
        <li><strong>Format:</strong> Click the **Format Text** button to generate the output.</li>
        <li><strong>Review:</strong>
            <ul>
                <li>Check the **Formatted HTML Code Output** for the generated <span class="highlight">&lt;div&gt;</span> or <span class="highlight">&lt;p&gt;</span> tag.</li>
                <li>Review the **Non-English Characters Highlighted** area for a character-by-character breakdown and confirmation of applied fonts (hover for details).</li>
                <li>Examine the final **Preview Email** area.</li>
            </ul>
        </li>
        <li><strong>Copy:</strong> Click the **Copy Code** button to copy the formatted HTML to your clipboard for use in your email or web project.</li>
    </ol>

    <h2>Technical Details and Limitations</h2>
    <ul>
        <li><strong>Font Hierarchy:</strong> The outermost tag (<span class="highlight">&lt;p&gt;</span> or <span class="highlight">&lt;div&gt;</span>) sets the language-specific font. ASCII/Latin characters are assumed to be best rendered by <span class="highlight">'Segoe UI'</span> and are explicitly wrapped where necessary (currently only for **Japanese**).</li>
        <li><strong>Line Breaks:</strong> All newline characters (<span class="highlight">\n</span>) in the input text are converted to the email-friendly HTML tag <span class="highlight">&lt;br /&gt;</span>.</li>
        <li><strong>Plain Text Only:</strong> The application only accepts plain text input. Any existing HTML styling, images, or formatting will be lost or interpreted as plain text.</li>
        <li><strong>No External Styling:</strong> The application only applies <span class="highlight">font-family</span> and <span class="highlight">font-size</span> via inline styles. It does not apply any other styling like <span class="highlight">padding</span>, <span class="highlight">margin</span>, or <span class="highlight">color</span>.</li>
    </ul>

</body>
</html>
