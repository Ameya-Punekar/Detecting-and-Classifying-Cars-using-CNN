
This project implements a Convolutional Neural Network (CNN) for detecting cars in grayscale images using a sliding window approach. The model is trained to classify windows containing cars and outputs precise coordinates for detected regions in test images.

---

## Project Structure

- **`CarData/`**: Contains training, validation, and test images.
  - `TrainImages/`: Images for training the model.
  - `TestImages/`: Images for testing the model.
  - `foundLocations.txt`: Output file with detected coordinates.
  - `Readme.md`: Detailed instructions on testing metrics.

- **`car_classifier_model1.pth`**: Trained CNN model weights.

---

## How It Works

1. **Model Architecture**:
   - A CNN-based binary classifier is trained to distinguish between car and non-car regions in images.

2. **Sliding Window**:
   - A sliding window of size `40x100` moves across the test images.
   - Each window is classified as containing a car or not using the trained model.

3. **Non-Maximum Suppression (NMS)**:
   - Overlapping bounding boxes are filtered to retain the most confident detections.

4. **Output**:
   - Detected car coordinates are saved in `foundLocations.txt`.

---

To properly evaluate the model's performance on the test data, please follow the instructions outlined in the `Readme.md` file within the `CarData` folder.
