# LICENSE-PLATE-RECOGNITION SYSTEM

*An Advanced System for License Plate Recognition*

This system is designed to detect and recognize two types of license plates commonly found in Vietnam: rectangular plates and square plates.

## Abstract

This system is capable of detecting and recognizing license plates from various sources, including images, videos, and webcams. Within the scope of this project, the camera's position is fixed, and only one vehicle can pass through the gate at a time. As a result, the system is designed to detect a single license plate per frame.

## Methodology

1. **Plate Detection**
   - Utilized the Sobel X operator for detecting vertical edges, followed by a morphological transformation.
   - Identified contours that meet the plate's aspect ratio to locate potential plates.
   - Verified the presence of characters on the identified plates to confirm them as license plates.

2. **Plate Recognition**
   - For character recognition, MobileNet_v1_0.5_128 was selected due to its lightweight nature, making it ideal for real-time recognition.

## Requirements

- Python 3.6
- To install the necessary dependencies, run: `pip install -r requirements.txt`

## Implementation

- To test on a video, execute `test.py`.
- To test on an image, execute `test_image.py`.

## Results

- ![Demo](<https://github.com/gautamankoji/LICENSE-PLATE-RECOGNITION-SYSTEM/blob/master/test_videos/screenshot_1.png>)
- ![Demo2](<https://github.com/gautamankoji/LICENSE-PLATE-RECOGNITION-SYSTEM/blob/master/test_videos/screenshot_2.png>)

## Notes

- For optimal implementation in your specific use case, consider adjusting the parameters: `minPlateArea`, `maxPlateArea`, and `ksize` in the `cv2.getStructuringElement` function.
