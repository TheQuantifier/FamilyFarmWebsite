README.txt – Roundelay Farm Website Instructions
------------------------------------------------

This file explains how to use and maintain the HTML, CSS, and JSON files used for the Roundelay Farm website.

------------------------------------------------
1. HTML Files (.html)
------------------------------------------------
- These are the core web pages of the site (e.g., index.html, about.html, contact.html, products.html, news.html).
- Each file defines the structure and content shown in the browser.
- Use these files to edit or create static sections specific to each page (e.g., headers, text, layout).
- When creating a new page, copy the structure from an existing HTML file and adjust the content as needed.

**Dynamic Content Pages:**
The following HTML pages load content dynamically from their corresponding JSON files in the `jsons/` folder. Avoid hardcoding their content in HTML—edit the relevant JSON instead:

- `news.html` → loads from `jsons/news.json`
- `products.html` → loads from `jsons/products.json`
- `contact.html` → loads from `jsons/contact.json`

------------------------------------------------
2. CSS File (common.css)
------------------------------------------------
- Shared styles for the entire site, including fonts, colors, spacing, layout, banners, navbars, and footers.
- Used by all HTML pages to maintain a consistent visual design.
- To update the appearance of elements globally (e.g., buttons, headings, links), make changes here.

------------------------------------------------
3. JSON Files (in /jsons/ folder)
------------------------------------------------

**news.json**
- Stores news stories displayed on the `news.html` page.
- Each entry includes a date, title, image, caption, and content.

Example:
{
  "date": "2023-06",
  "displayDate": "June 2023",
  "title": "Weather Eye",
  "image": "images/moon_riding_rainbow_IMG_0876_1000x750.jpg",
  "caption": "Moon riding a rainbow!",
  "content": "Everything is growing here in the highland rim of northern Tennessee..."
}

- Tips:
  • Use `"date"` in the format `YYYY-MM` for correct sorting.
  • Add newest stories to the top.
  • Ensure all entries are valid JSON (quotes around strings, commas between objects, no trailing commas).

**products.json**
- Stores product data for display on `products.html`.
- Each product typically includes: name, description, price, and one or more image file names.
- Edit this file to update or add new farm products.

**contact.json**
- Contains contact information shown on the `contact.html` page.
- Includes:
  • `phone`: phone numbers by type (e.g., mobile, landline)
  • `email`: one or more email addresses
  • `hours`: business hours by weekday
  • `pickup`: address, description, and embedded map info
  • `social`: social media links (optional)

------------------------------------------------
4. Images
------------------------------------------------
- Place all site images inside the `/images/` folder.
- Use descriptive file names to match image references in HTML and JSON files.
- Ensure images are appropriately sized for the web to optimize loading time.

------------------------------------------------
5. Editing & Testing Notes
------------------------------------------------
- Always test changes in a browser to verify formatting and functionality.
- Avoid editing the JavaScript inside `news.html`, `products.html`, or `contact.html` unless you are comfortable working with dynamic content loading.
- When making layout or style changes, confirm they look good across multiple screen sizes.

------------------------------------------------
Folder Structure Overview:
------------------------------------------------
/images/         → All banner and content images  
/jsons/          → JSON files: contact.json, news.json, products.json  
common.css       → Shared styles  
index.html       → Home page  
about.html       → About the farm  
contact.html     → Contact info and form  
news.html        → News stories (uses news.json)  
products.html    → Products listing (uses products.json)

End of README