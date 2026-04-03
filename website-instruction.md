# Website Content Extraction Specification

## Objective
Create a structured Markdown (`.md`) file that extracts and organizes all textual and content elements from the website’s HTML into a clean, editable format.

This Markdown file will serve as the **single source of truth** for all editable website content. Future modifications will be made in this file and reflected back into the website.

---

## Requirements

### 1. Hierarchical Structure
- Represent the website structure clearly using Markdown headings:
  - `#` for main sections
  - `##` for subsections
  - `###` for components
- The structure should reflect the actual layout of the webpage.

---

### 2. Content Classification
For each content element, explicitly specify its type:

- Title / Heading
- Paragraph / Body Text
- Image
- Video
- Button / Label
- Table
- Caption
- Navigation / Menu
- Footer
- Other UI components (if applicable)

---

### 3. Raw Text Preservation
- Extract and include the **exact original text** from the HTML.
- Do **not** paraphrase, summarize, or modify any content.

---

### 4. HTML Mapping (Recommended)
- Include references to the original HTML elements when possible.
- Example:
  - Tag name
  - Class name
  - ID

This helps map Markdown content back to the website.

---

### 5. Media Handling
For images and videos, include:

- Source path or URL
- Alt text (for images)
- Captions or descriptions (if available)

---

### 6. Standard Content Block Format

Each content element should follow a consistent structure:

#### Example

```markdown
### Section: Hero

- Type: Title  
  HTML: `<h1 class="hero-title">`  
  Content: "Your Original Title Here"

- Type: Paragraph  
  HTML: `<p class="hero-description">`  
  Content: "Your original paragraph text here."

- Type: Image  
  HTML: `<img src="..." alt="...">`  
  Source: `/images/hero.png`  
  Alt Text: "Hero image description"
```

---

## Deliverable: extracted content

The live site’s **visible copy** (and short notes for uncaptioned images/videos) lives in **`website-content.md`**. Use it as the **single source of truth** for wording; after editing, sync the same text into `index.html`. It intentionally omits HTML, meta tags, and other non-visible markup.