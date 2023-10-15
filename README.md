# KITTI Sensor Fusion and Object Detection

## Project Overview
This project aims to demonstrate a multi-sensor fusion approach for object localization and visualization by utilizing LiDAR, camera, and IMU data. The primary objective is to detect objects in 2D camera images, estimate their 3D positions using LiDAR data, and subsequently transform these positions into various coordinate frames including IMU and geodetic frames.

## Libraries Used
- `torch` library is utilized for running the YOLOv5 object detection model.
- `cv2` (OpenCV) is used for image processing and visualization tasks.
- `numpy` is employed for numerical operations.
- `pymap3d` is used for geodetic to cartesian coordinate transformations.
- `folium` is utilized for map-based visualization.
- `pandas` is employed for data manipulation.
- `matplotlib` is used for displaying images and plots.

## Key Features
1. **Loading Calibration Data**: This feature loads calibration data to establish transformations between sensor frames.
2. **Projection Matrices**: This feature computes matrices for transforming LiDAR points to camera coordinates and vice versa.
3. **Object Detection**: This feature utilizes YOLOv5 to detect objects in the camera images.
4. **LiDAR to Camera Projection**: This feature projects LiDAR points to camera frame and associates them with detected objects.
5. **Coordinate Transformations**: This feature transforms object coordinates to IMU and geodetic frames.
6. **Visualization**: 
    - Visualize object locations on a map using Folium.
    - Create a top-down view scenario showing the ego-vehicle and detected objects.
    - Visualize the LiDAR point cloud projected onto the camera image.
7. **Video Generation**: This feature generates a video showing the results over time.
8. **Validation**: This feature performs basic validation by comparing theoretical and actual IMU values.

## Usage
1. Ensure all required libraries are installed.
2. Download and prepare the KITTI dataset.
3. Run the provided script in a Jupyter Notebook environment to process the data, perform object localization, and create visualizations.

## Outputs
- A video file named `lidar_frame_stack.mp4` showing the object detection and localization results.
- Various visualizations including map-based object locations and top-down scenario view are generated.

## Further Enhancements
- Implementing additional validation steps could improve the robustness of object localization.
- Exploring different object detection models may yield better detection performance.
- Optimizing the performance for real-time processing could be a future direction to take this project towards.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
