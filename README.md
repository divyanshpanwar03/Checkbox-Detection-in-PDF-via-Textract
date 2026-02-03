📄 Audit PDF Checkbox & Issue Extraction

This project implements a layout-aware document processing pipeline to extract structured audit information from multi-page PDF documents. It automatically detects issue headings, checked checkboxes, and associates each checkbox with its correct issue and semantic meaning (Severity, Category, Root Cause).

The system is designed for audit and compliance reports where information is visually structured but not machine-readable.

🚀 What This Project Does

Converts multi-page PDFs into page-level images
Extracts text and checkboxes with positional information
Detects numbered issue headings
Assigns checkboxes to the correct issue using layout boundaries
Resolves single-character label ambiguity (C, F, O, etc.)
Supports multi-select fields (e.g. multiple Root Causes)
Prevents data leakage across issues and continuation pages
Produces clean, structured output for reporting

HIGH LEVEL FLOW

PDF
 ├── Split into pages
 ├── Extract text & checkboxes
 ├── Validate page structure
 ├── Detect issue headings
 ├── Define issue boundaries
 ├── Assign checkboxes to issues
 ├── Map checkboxes to labels
 └── Generate structured output

🛠️ Installation & Setup

1️⃣ Clone the Repository
2️⃣ Create a Virtual Environment (Recommended)
3️⃣ Install Python Dependencies
4️⃣ Install System Dependency (PDF to Image)

▶️ How to Run the Project
1️⃣ Place your PDF file inside the project folder (or update the path in code).
2️⃣ Update the PDF path in main.py:
3️⃣ Run the pipeline

📤 Output Format

The output is printed as structured data per page and per issue.

⚙️ Configuration Notes

Issue detection is layout-based, not text-only
Severity is treated as single-select
Category and Root Cause support multi-select
Continuation pages are automatically handled
No page numbers or hardcoded coordinates are used.

🧪 Known Limitations

Works best on digitally generated PDFs
Assumes left-to-right checkbox layout
Not designed for handwritten or scanned forms
Very different templates may require rule tuning

📌 Summary
This project demonstrates how layout-aware document processing can reliably convert complex audit PDFs into structured,
machine-readable data using geometry and rule-based logic instead of fragile OCR heuristics.
