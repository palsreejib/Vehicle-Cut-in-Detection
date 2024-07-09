# Vehicle-Cut-in-Detection

Vehicle cut-in detection is a deep learning model that estimates the time to collision (TTC) between vehicles in urban driving scenarios, aiding in accident avoidance.

## Project Description

The project report introduces a deep learning method for vehicle cut-in detection, focusing on transfer learning. It aims to recognize real-time situations for drivers and autonomous vehicles' decision-making systems. The system includes object recognition, tracking, speed calculation, and time-to-collision estimation. The report details methodology, datasets, implementation, results, challenges, strategies, and potential improvements.

### Object Recognition and Tracking:

The YOLOv8.pt model, fine-tuned using transfer learning, was used for vehicle detection on the India Driving Dataset (IDD) to identify different vehicle types in diverse traffic scenarios, with a tracking algorithm to maintain trajectories across frames.

### Speed Calculation

Vehicle speeds are determined by analyzing position changes across consecutive frames, converting pixel coordinates to real-world coordinates, calculating displacement, and computing speed based on frame rate, with a smoothing filter applied for accuracy.

### Time-to-Collision

The Total Time to Collision (TTC) is calculated by analyzing the lateral distance and relative velocity between the ego and potential cut-in vehicles, using lane detection algorithms to estimate the ego vehicle's position and implementing a prediction model.
`TTC = distance/speed`
