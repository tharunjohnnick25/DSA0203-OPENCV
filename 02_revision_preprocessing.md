# AT2 CO5 – OCR-Based Document Text Extraction
## Revision 2 – Preprocessing Added

### Aim
Improve the OCR design by adding document preprocessing before text recognition.

### Structured Pseudocode
1. START
2. Read the input document image.
3. IF the image cannot be loaded:
   - Display an error message.
   - STOP.
4. Check the document image dimensions.
5. Resize the image while preserving its aspect ratio.
6. Convert the resized image to grayscale.
7. Apply Gaussian or median filtering to reduce noise.
8. Enhance document contrast.
9. Apply global or adaptive thresholding.
10. Generate the binary document image.
11. Send the processed image to the OCR engine.
12. Extract the recognized text.
13. Display the extracted text.
14. Save the extracted text.
15. END.
