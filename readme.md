# Stitch Coding Exercise

I focused on more modern email service providers and clients for this exercise, due to workload and time constraints. 

You can view the Litmus test results here: https://litmus.com/pub/10B0xcnOAAko17cY 

If this were a real world client, and I was at Stitch, I would be asking a lot of clarifying questions, such as:

## Questions & Notes for the Team

### Audience & Accessibility
- Do we know which email clients the audience uses?  
- Audience's age / general makeup? (Accessibility concerns) 

### Coding Standards
- What’s the team’s approach: pixel-perfect rendering in all clients or cleaner, more maintainable code?  
- Do we have a standard Email Client Support List?

### Assets
- Image assets were not provided at 2x.  
- Photoshop file is 1x resolution.  

### Source of Truth
- Should we follow the Excel file or the PSD?  
- See noted discrepancies below.  

### Mobile Layout
- No mobile design was provided — current mobile layout is me trying to adhere to best practices.  

### Accessibility Details
- **Button contrast** (Modules 3 & 6):  
  - “Read more” button fails WCAG AA/AAA (Contrast ratio: 1.34:1 per WebAIM): https://webaim.org/resources/contrastchecker/ 
  - I increased contrast in my file.
- **Hero Headline:** 
  - Was provided as an image slice, which is not good accessibility practice.
  - I converted to live `<h1>` text.  
- **Alt text (Modules 2 & 4)** 
  - Excel alt text duplicates headlines, so I left decorative images blank to avoid redundancy. 
  - This information would be read 2x in a row by the screen reader.

### Braze Attributes
- Confirm personalization syntax. Currently using: `{{${first_name}, | default: 'Hi there,'}}`
  - Fallback, in case there is no first_name attribute, is `Hi there,`
  - I kept the file format as .html since this is the ONLY liquid in the whole file.

---

## PSD vs. Excel Discrepancies
- Nav menu font: PSD uses *Open Sans*; Excel does not list this.  
- Excel file includes two “Module 7” sections.  
- Capitalization differs between PSD and Excel.  
- Some button/link copy missing from Excel.  
