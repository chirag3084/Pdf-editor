# 📝 Django PDF Editor & Converter

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Django](https://img.shields.io/badge/Django-3.x%2B-green)
![License](https://img.shields.io/badge/License-MIT-orange)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

A comprehensive, web-based PDF manipulation tool built with **Django** and powerful **JavaScript libraries**. This application serves as a complete suite for editing, annotated, converting, and compressing PDF documents directly within the browser.

---

## 📸 Screenshots

![Dashboard Interface](/path/to/dashboard-screenshot.png)
*The main editing interface featuring the toolbar and canvas.*

---

## ✨ Key Features

### 🎨 PDF Editing Suite
* **Add Text**: Insert custom text blocks with adjustable fonts, sizes, and colors.
* **Insert Images**: Seamlessly overlay images (JPG, PNG) onto existing PDF pages.
* **Freehand Drawing**: Draw, sign, or annotate freely using the drawing tool.
* **Highlight & Erase**: Highlight key areas or remove unwanted content with a configurable eraser.
* **Navigation & Zoom**: Intuitive page navigation and zoom controls for detailed editing.

### 🔄 Conversion Tools
* **PDF to Word**: Convert documents to editable `.docx` files.
* **PDF to Excel**: Extract tables and data into `.xlsx` format.
* **PDF to Image**: Render PDF pages as high-quality images.

### 🛠️ Utilities
* **Compression**: Reduce file size for images and PDFs without significant quality loss.
* **Undo/Redo**: Full history support to revert or re-apply changes.
* **Export Options**: Download modified files instantly.

---

## 🏗️ Tech Stack

| Category | Technology | Purpose |
| :--- | :--- | :--- |
| **Backend** | **Django** (Python) | Server-side logic, routing, and file handling. |
| **Frontend** | **HTML5 / CSS3** | Structure and styling. |
| **Scripting** | **JavaScript (ES6+)** | DOM manipulation and logic. |
| **Rendering** | **PDF.js** | Rendering PDF pages in the browser. |
| **Canvas** | **Fabric.js** | Object manipulation (text, drawing, shapes) on HTML5 Canvas. |
| **Manipulation** | **PDFLib** | Modifying the actual PDF structure (merging, embedding). |
| **Utilities** | **Compressor.js** | Client-side image compression. |
| **Conversion** | **docx** / **ExcelJS** | Generating Word and Excel documents from JS. |

---

## 🚀 Setup and Installation

Follow these steps to get a local copy up and running.

### Prerequisites
* [Python 3.8+](https://www.python.org/downloads/)
* [Node.js](https://nodejs.org/) (Optional, only if managing frontend packages via npm)

### Step-by-Step Guide

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/your-username/pdf-editor.git](https://github.com/your-username/pdf-editor.git)
    cd pdf-editor
    ```

2.  **Create Virtual Environment**
    ```bash
    # Windows
    python -m venv venv
    venv\Scripts\activate

    # macOS/Linux
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: Ensure your `requirements.txt` contains `Django`, `Pillow`, and any other backend libs)*

4.  **Apply Database Migrations**
    ```bash
    python manage.py migrate
    ```

5.  **Run the Server**
    ```bash
    python manage.py runserver
    ```

6.  **Access the App**
    Open your browser and navigate to: `http://127.0.0.1:8000`

---

## 📦 Frontend Integration

This project currently utilizes CDNs for simplicity. Ensure your base HTML template (`base.html` or `index.html`) includes the following:

```html
<script src="[https://cdnjs.cloudflare.com/ajax/libs/jquery/3.5.1/jquery.min.js](https://cdnjs.cloudflare.com/ajax/libs/jquery/3.5.1/jquery.min.js)"></script>
<script src="[https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.5.207/pdf.min.js](https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.5.207/pdf.min.js)"></script>
<script src="[https://cdnjs.cloudflare.com/ajax/libs/fabric.js/4.3.1/fabric.min.js](https://cdnjs.cloudflare.com/ajax/libs/fabric.js/4.3.1/fabric.min.js)"></script>

<script src="[https://cdnjs.cloudflare.com/ajax/libs/pdf-lib/1.17.1/pdf-lib.min.js](https://cdnjs.cloudflare.com/ajax/libs/pdf-lib/1.17.1/pdf-lib.min.js)"></script>
<script src="[https://cdn.jsdelivr.net/npm/compressorjs@1.0.7/dist/compressor.min.js](https://cdn.jsdelivr.net/npm/compressorjs@1.0.7/dist/compressor.min.js)"></script>

<script src="[https://cdnjs.cloudflare.com/ajax/libs/docx/6.0.3/docx.min.js](https://cdnjs.cloudflare.com/ajax/libs/docx/6.0.3/docx.min.js)"></script>
<script src="[https://cdnjs.cloudflare.com/ajax/libs/exceljs/4.2.1/exceljs.min.js](https://cdnjs.cloudflare.com/ajax/libs/exceljs/4.2.1/exceljs.min.js)"></script>
