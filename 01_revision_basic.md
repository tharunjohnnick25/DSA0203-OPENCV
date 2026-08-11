# AT2 CO5 – OCR-Based Document Text Extraction
## Revision 1 – Basic OCR Design

### Aim
Design a basic pseudocode routine for extracting text from a document image.

### Structured Pseudocode
1. START
2. Read the input document image.
3. IF the image cannot be loaded:
   - Display an error message.
   - STOP.
4. Convert the document image to grayscale.
5. Apply thresholding to separate text from the background.
6. Send the processed image to the OCR engine.
7. Extract the recognized text.
8. Display the extracted text.
9. Save the extracted text.
10. END.
