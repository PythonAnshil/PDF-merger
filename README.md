# PDF-merger
This project is a simple Python script to merge multiple PDF files in a directory into a single PDF. It uses the PyPDF2 library to perform the PDF merging.

Features

Automatically merges all PDF files in the current directory.

Simple and efficient code.

Requirements

Python 3.x

PyPDF2 library

Installation

To run this script, make sure Python is installed. You also need to install the PyPDF2 library. You can install it via pip:

pip install PyPDF2

Usage

Clone or download this repository.

Place all the PDF files you want to merge in the same directory as the script.

Run the script:

python pdf_merger.py

The script will merge all PDF files in the directory and create a new file called merged-pdf.pdf.

Code Explanation

from PyPDF2 import PdfWriter
import os

merger = PdfWriter()
files = [file for file in os.listdir() if file.endswith(".pdf")]

for pdf in files:
    merger.append(pdf)

merger.write("merged-pdf.pdf")
merger.close()

Import Libraries: The script imports PdfWriter from PyPDF2 to handle PDF merging, and os to list files in the directory.

Create PdfWriter Instance: merger = PdfWriter() creates an instance for handling the merge.

Find All PDF Files: files = [file for file in os.listdir() if file.endswith(".pdf")] lists all PDF files in the current directory.

Merge PDFs: The script iterates over the list of PDF files and appends them to the merger instance.

Write Output File: merger.write("merged-pdf.pdf") writes the merged PDF to a new file.

Contributing

Feel free to fork this repository, make improvements, and submit a pull request. Any contributions are welcome!

License

This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments

Thanks to the creators of PyPDF2 for providing a great tool for working with PDF files.