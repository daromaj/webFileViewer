# webFileViewer <a href="https://github.com/daromaj/webFileViewer" target="_blank"><img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub" width="24" height="24"></a>

## Live Demo

You can try the live version of the tool here: [https://daromaj.github.io/webFileViewer/](https://daromaj.github.io/webFileViewer/)

## Overview
This project provides three client-side HTML-based parsers for handling document files directly in the browser without server interaction:

1. **docx-parser.html** - DOCX document parser
2. **xlsx-parser.html** - XLSX spreadsheet parser
3. **msg-parser.html** - MSG email container parser

All parsers support file processing entirely in the browser with capabilities for content extraction and embedded file handling.

## Key Features

### DOCX Parser (docx-parser.html)
- ✅ Extracts raw text content from Word documents
- ✅ Identifies and lists embedded files (images, documents, etc.)
- ✅ Preserves original file structure in downloads
- ✅ Handles complex document formatting
- 📁 Embedded files path: `word/embeddings/`

### XLSX Parser (xlsx-parser.html)
- ✅ Converts spreadsheet data to JSON format
- ✅ Extracts embedded files from Excel workbooks
- ✅ Maintains original file names in downloads
- ✅ Supports both formula and value-based content
- 📁 Embedded files path: `xl/embeddings/`

### MSG Parser (msg-parser.html)
- ✅ Parses email metadata (sender, recipient, date, subject)
- ✅ Renders HTML/plain text email body content
- ✅ Extracts and enables download of all attachments
- ✅ Preserves attachment file names and types
- 📄 Supports both embedded and file attachments

## Technical Implementation
- **Client-side Processing**: All operations occur in the browser with no data transmission
- **Libraries Used**:
  - DOCX: `docxtemplater` + `jszip`
  - XLSX: `xlsx` + `jszip`
  - MSG: `msg.reader`
- **File Size**: Optimized for files under 1GB (browser memory limitations)
- **Embedded File Handling**: Uses Blob URLs for safe, direct downloads

## Usage Instructions
1. Open the desired parser HTML file in a modern web browser
2. Upload the corresponding file type (.docx, .xlsx, or .msg)
3. View extracted content in the designated output area
4. Download embedded files/attachments using generated links

## Limitations
- 📉 Performance may degrade with files approaching 1GB size
- 🔒 Does not support password-protected files
- 🖼️ Image rendering requires proper browser MIME type support
- 📅 Date formatting depends on browser locale settings

## Security Considerations
- All processing occurs locally in the browser
- No data is transmitted to external servers
- Embedded file downloads require explicit user action
