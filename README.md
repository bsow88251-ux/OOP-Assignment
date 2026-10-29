# Crop Yield Monitor

A simple Python project demonstrating **Object-Oriented Programming (OOP)** concepts through an agricultural productivity tracker.

# Overview
This project is a **Crop Yield Monitor** application built with Python to showcase:
- Classes & Objects
- Instance methods
- Class methods
- Data storage in lists
- Basic input validation


# Classes

# 1. `CropRecord`
Represents a single crop record.
- **Attributes**:
  - `record_id` – unique identifier
  - `crop_name` – name of the crop
  - `area` – area in hectares
  - `harvest` – harvest in tonnes
- **Method**:
  - `show_record()` → calculates productivity (`harvest / area`) and prints details.

# 2. `CropMonitor`
Manages multiple crop records.
- **Class Attribute**: `app_name = "Crop Yield Monitor"`
- **Class Method**: `show_app_name()` → prints the app name.
- **Functions**:
  - `add_record(monitor, record)` → adds a `CropRecord` to the list
  - `display_records(monitor)` → shows all records or a message if none exist.


# Program Flow
The program runs an interactive menu loop:
1. **Add a crop record** – prompts for ID, crop name, area, and harvest; validates input before creating a `CropRecord`.
2. **Display all records** – lists all stored crop records.
3. **Search by record ID** – finds and displays a record by its ID, or shows “Record not found”.
4. **Exit** – ends the program with a goodbye message.


# Input Validation
- Ensures `area > 0`
- Ensures `harvest ≥ 0`
- Handles invalid numeric input with error messages.

Alignment with DPG Standards
This solution aligns with Digital Public Goods (DPG) Standards in the following ways:

Open Source: Shared publicly under an open license for reuse and collaboration.

Documentation: Clear README and inline comments make the solution replicable.

Reusability & Interoperability: Modular design allows easy extension for other agricultural systems.

Data Privacy & Security: Handles only crop-related data, no personal information.

Inclusivity & Accessibility: Lightweight, runs on basic Python environments, adaptable for low-resource settings.

Sustainability: Promotes open standards and simple design for long-term community use.

#How to Run
Clone the repository and run the program:

```bash
git clone https://github.com/bsow88251-ux/OOP-Assignment.git
cd OOP-Assignment/python
python main.py
