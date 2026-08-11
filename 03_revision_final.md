# AT2 CO5 – OCR-Based Document Text Extraction
## Revision 3 – Final Structured Design

### Aim
Design a complete structured pseudocode routine for OCR-based document text extraction using image preprocessing, text-region handling, OCR, validation, and output generation.

### Input
- Scanned document image
- JPG, JPEG, PNG, or page image extracted from PDF

### Output
- Extracted and cleaned text
- Preprocessed document image
- Saved text file

### Structured Pseudocode

#### Step 1 – Initialize
1. START.
2. Initialize the input document path.
3. Initialize image-processing parameters.
4. Initialize the OCR engine.
5. Define the output text-file path.

#### Step 2 – Read Document
6. Read the input document image.
7. IF the image cannot be loaded:
   - Display an error message.
   - STOP.
8. ELSE continue processing.

#### Step 3 – Resize Document
9. Determine the document dimensions.
10. IF the document is too small:
    - Increase its resolution.
11. IF the document is excessively large:
    - Resize while preserving aspect ratio.
12. Store the resized image.

#### Step 4 – Convert to Grayscale
13. Convert the document from color to grayscale.
14. Store the grayscale image.

#### Step 5 – Remove Noise
15. Apply Gaussian or median filtering.
16. Reduce scanner noise and small image artifacts.
17. Store the denoised image.

#### Step 6 – Enhance Contrast
18. Analyze the grayscale intensity distribution.
19. Apply contrast enhancement when required.
20. Improve separation between text and background.

#### Step 7 – Binarize
21. Determine the document illumination condition.
22. IF illumination is uniform:
    - Apply global thresholding.
23. ELSE:
    - Apply adaptive thresholding.
24. Generate the binary document image.

#### Step 8 – Morphological Cleaning
25. Inspect the binary image for small artifacts.
26. Apply morphological opening to remove small noise.
27. Apply morphological closing to connect broken text regions.
28. Store the cleaned image.

#### Step 9 – Correct Orientation
29. Estimate the document or text-line orientation.
30. IF the document is rotated:
    - Calculate the rotation angle.
    - Rotate the document.
31. Store the orientation-corrected image.

#### Step 10 – Detect Text Regions
32. Identify regions containing text.
33. Remove obvious non-text regions when required.
34. Arrange text regions in reading order.

#### Step 11 – OCR Processing
35. Send the processed document to the OCR engine.
36. Configure OCR according to the expected document layout.
37. Perform character and word recognition.
38. Store the recognized text.

#### Step 12 – Post-Process Text
39. Remove unnecessary spaces.
40. Remove obvious OCR artifacts.
41. Normalize line breaks and formatting.
42. Preserve meaningful words, sentences, and paragraphs.
43. Store the cleaned text.

#### Step 13 – Validate Result
44. Check whether meaningful text was extracted.
45. IF no meaningful text is detected:
    - Display an OCR failure message.
    - Recommend better image quality or preprocessing parameters.
46. ELSE continue to output generation.

#### Step 14 – Generate Output
47. Display the original document.
48. Display the preprocessed document.
49. Display the extracted text.
50. Save the extracted text to a text file.
51. Save the preprocessed image if required.

#### Step 15 – Terminate
52. Release resources.
53. Display a successful completion message.
54. END.

### Final Workflow
INPUT DOCUMENT
↓
READ IMAGE
↓
RESIZE
↓
GRAYSCALE
↓
NOISE REMOVAL
↓
CONTRAST ENHANCEMENT
↓
THRESHOLDING
↓
MORPHOLOGICAL CLEANING
↓
ORIENTATION CORRECTION
↓
TEXT REGION DETECTION
↓
OCR
↓
TEXT POST-PROCESSING
↓
VALIDATION
↓
SAVE / DISPLAY TEXT
↓
END
