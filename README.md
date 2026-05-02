# NLP Document Processing (RegEX and NER)

## Overview

This notebook demonstrates the development of an intelligent document-processing pipeline using Python and Natural Language Processing (NLP). The primary objective was to extract structured information from unstructured text such as invoices, receipts, and business documents.

By combining regular expressions with spaCy's Named Entity Recognition (NER), the notebook transforms raw textual data into machine-readable structured outputs suitable for automation, analytics, and downstream business applications.

---

## Objectives

* Extract key information from textual documents.
* Identify and normalize dates, monetary values, and invoice numbers.
* Detect named entities such as people, organizations, locations, dates, and monetary amounts.
* Visualize recognized entities for analysis and debugging.
* Build a reusable document-processing pipeline.
* Export extracted results in JSON format for integration with other systems.

---

## Technologies and Libraries Used

* **Python** – Core programming language.
* **re (Regular Expressions)** – Pattern-based text extraction.
* **spaCy** – Industrial-strength NLP library.
* **displaCy** – Visualization tool for named entities.
* **JSON** – Structured data storage and exchange.

---

## Major Components Implemented

### 1. Date Extraction

A custom function was developed to identify dates in multiple formats, including:

* `MM/DD/YYYY`
* `DD-MM-YYYY`
* `Month DD, YYYY`
* `YYYY-MM-DD` (ISO format)

This enables robust handling of dates commonly found in invoices and business documents.

---

### 2. Monetary Amount Extraction

A regex-based parser was implemented to extract currency values from text, supporting formats such as:

* `$1,250.50`
* `$1250`
* `112.45`

Extracted values were cleaned and converted into floating-point numbers for numerical processing.

---

### 3. Invoice Number Extraction

A flexible invoice identifier extractor was built to recognize multiple invoice formats, including:

* `INV-2024-001`
* `#12345`
* `ORDER-ABC123`
* `Invoice Number: XYZ123`

This ensures compatibility across different invoice templates and naming conventions.

---

### 4. Named Entity Recognition (NER)

Using spaCy, the notebook extracts important business entities from text, including:

* **Persons**
* **Organizations**
* **Locations**
* **Dates**
* **Monetary Values**

This converts unstructured text into structured semantic information.

---

### 5. Entity Visualization

Named entities were visually highlighted using spaCy's `displacy` renderer. This provided:

* Interactive in-notebook visualization
* HTML export for external viewing and reporting
* Improved interpretability and debugging of NER results

---

### 6. Document Processing Pipeline

A consolidated processing function was created to:

* Accept raw document text
* Apply all extraction modules
* Aggregate results into a structured dictionary
* Standardize output format

This modular design improves reusability and scalability.

---

### 7. JSON Export

The final extracted information was serialized into JSON format, enabling:

* Easy storage
* API integration
* Database ingestion
* Interoperability with external systems

---

## Sample Information Extracted

The pipeline can successfully identify:

* Invoice numbers
* Dates
* Monetary amounts
* Customer or vendor names
* Organizations
* Geographic locations

---

## Key Learning Outcomes

* Practical use of regular expressions for pattern matching.
* Application of spaCy for industrial NLP tasks.
* Understanding of Named Entity Recognition (NER).
* Techniques for extracting structured data from unstructured text.
* Building modular and reusable NLP pipelines.
* Exporting processed data in JSON format.
* Visualizing NLP outputs for validation and presentation.

---

## Real-World Applications

* Invoice automation
* Receipt processing
* Financial document analysis
* Intelligent document processing (IDP)
* Business process automation
* Data extraction for ERP systems
* OCR post-processing pipelines

---

## Conclusion

This notebook successfully demonstrates the design and implementation of an end-to-end NLP-based document information extraction system. By integrating rule-based methods with machine learning-driven entity recognition, the solution achieves both flexibility and accuracy.

The resulting pipeline provides a strong foundation for real-world intelligent document processing applications, particularly in finance, accounting, and enterprise automation domains.

It can be further extended with OCR integration, document classification, validation rules, and deployment as an API or production-ready application.
