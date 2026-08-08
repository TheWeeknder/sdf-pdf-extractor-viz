# SDF Document Field Extractor & Visualizer

This project provides an automated pipeline for identifying, extracting, and visually verifying key fields from Standard Document Format (SDF) PDFs. It utilizes **PyMuPDF** for coordinate-aware text extraction and **OpenCV** for bounding-box verification.

## Features
*   **Multi-Page Extraction:** Iterates through complex document structures to capture data across all pages.
*   **Coordinate-Based Parsing:** Extracts text along with precise `bbox` coordinates (x0, y0, x1, y1).
*   **Key Field Identification:** Specifically tuned to extract:
    *   Vendor Information (e.g., Cytiva)
    *   Dates (Effective, Manufacturing, Expiration)
    *   Document Revision and Instruction references.
    *   Table-based batch/product codes.
*   **Visual Verification:** Automatically draws bounding boxes around extracted fields on the document images for auditing and QA.
*   **Structured Output:** Generates a clean JSON-like list of dictionaries containing the text and its location.

## Tech Stack
*   **Python 3.x**
*   **PyMuPDF (fitz):** For high-performance PDF parsing.
*   **OpenCV:** For image processing and annotation.
*   **Pandas:** For data summarization.
*   **Regex:** For pattern-based field matching.

## Usage
1. Place your PDF in the project directory.
2. Run the extraction script to generate a structured summary.
3. View the generated images to verify that the bounding boxes correctly align with the target text.
