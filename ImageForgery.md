# Problem Statement:

Develop a machine learning model to detect and classify image forgeries while highlighting the manipulated regions. The model should not only distinguish genuine images from tampered ones but also localize the specific areas of alteration, ensuring efficient handling of high-resolution images across various formats and manipulations.

---
## Key Components:

1. The solution must be able to classify whether an image is genuine or manipulated.
2. Highlight the forged regions by drawing bounding boxes or using segmentation techniques to identify specific areas of manipulation.
3. Support batch processing for large datasets of images.
4. Provide a confidence score for each prediction.
5. Can handle varying lightning conditions in genuine image eg flash on while clicking the picture.
6. Handling images with different resolutions, compression levels, and common image formats (JPEG, PNG, etc.).
  
---
## Examples:
1. **Image Retouching**:
   - Subtle edits to enhance or alter specific features without overt manipulation like text manipulation etc.
   - The model should recognize and highlight these subtle modifications.
   -<p align="center">
     <img src="https://github.com/user-attachments/assets/7241223c-d297-48b3-a296-701dba1c0204" alt="Another Forgery Type" width="300" height="200">
     <img src="https://github.com/user-attachments/assets/b987574c-de74-4683-b1eb-f74902729f62" alt="Another Forgery Type" width="300" height="200">
     <img src="https://github.com/user-attachments/assets/68bdabc1-b1a4-4715-a550-fac01a34eb9a" alt="Another Forgery Type" width="300" height="200">
     </p>
2. **Splicing**:
   - Two unrelated images are combined (e.g., placing a person from one image into a different background).
   - The model should identify regions from different sources and highlight these areas.
   - <img src="https://github.com/user-attachments/assets/4ef0810e-0c9f-4c98-b49e-1dc661cc5726" alt="Splicing Forgery" width="500" height="200">
3. **Copy-Move Forgery**:
   - A part of the image (e.g., a car) is copied and pasted elsewhere in the same image.
   - Model should detect duplicate regions and localize them by highlighting.
   - <img src="https://github.com/user-attachments/assets/b41905ff-666e-4c53-8c7b-0274f89922e0" alt="Copy-Move Forgery" height="200">


---
## Model Evaluation Criteria:
1. **Accuracy**:
   - Ability to correctly classify images as genuine or manipulated.
2. **Localization Precision**:
   - Precision in detecting and highlighting the forged regions (measured using metrics like Intersection over Union (IoU)).
3. **Confidence Score**:
   - Provide reliable confidence scores for forgeries and localization task.
4. **Processing Efficiency**:
   - Speed and scalability in handling large image datasets, including time per batch and overall processing time.
5. **Performance in different Environmental Conditions**:
   - Performance with varying lightning conditions in genuine image eg flash on while clicking the picture.
6. **Bonus**:
   - Detect if the image is AI generated.

## Dataset:
Feel free to explore datasets with listed forgeries. You will be judged based on our custom created sample that contains forged and authentic images.
