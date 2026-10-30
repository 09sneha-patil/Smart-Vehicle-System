# Smart Vehicle System – AI-Based Driver Drowsiness and Obstacle Detection

## 1. Project Overview

The **Smart Vehicle System** is an AI-powered driver safety application developed to improve road safety by monitoring driver alertness and detecting potential obstacles on the road. The system uses computer vision and machine learning techniques to identify signs of driver fatigue and provide timely alerts when potentially dangerous situations are detected.

The application combines real-time camera-based monitoring, drowsiness detection, obstacle detection, audio warning mechanisms, and a web-based dashboard to provide an integrated vehicle safety monitoring experience.

The primary goal of this project is to minimize the risk of accidents caused by driver drowsiness and unexpected road obstacles by providing continuous monitoring and early warnings.

## 2. Problem Statement

Driver fatigue and lack of attention are major factors contributing to road accidents. Drivers may become sleepy during long journeys, reducing their reaction time and awareness of surrounding conditions. Similarly, obstacles on the road can create dangerous situations if they are not identified in time.

Traditional driving practices depend heavily on the driver's ability to recognize these situations. Therefore, an intelligent monitoring system is needed to detect signs of fatigue, identify potential obstacles, and alert the driver before the situation becomes more dangerous.

This project addresses these challenges through computer vision-based monitoring and an interactive safety dashboard.

## 3. Project Objectives

- Develop an intelligent system for monitoring driver alertness.
- Detect drowsiness using facial landmark detection and eye movement analysis.
- Identify potential road obstacles through camera-based detection.
- Generate audio and visual alerts to notify drivers about unsafe conditions.
- Provide trip monitoring and safety analytics through a web dashboard.
- Support vehicle management through a fleet management module.
- Improve driver awareness through real-time monitoring and safety indicators.

## 4. Key Features and Functionalities

### A. Driver Drowsiness Detection

The drowsiness detection module continuously monitors the driver's face using a camera and analyzes eye movements to identify signs of fatigue.

The system uses OpenCV and Dlib's 68-point facial landmark model to detect important facial regions, particularly the eyes.

It calculates the **Eye Aspect Ratio (EAR)** to estimate whether the driver's eyes are open or closed.

- When the EAR is above the configured threshold, the eyes are considered open.
- When the EAR falls below the configured threshold, the system identifies a possible eye-closure condition.
- If the condition continues for a specified number of consecutive frames, the system detects possible drowsiness.

The configured EAR threshold is 0.25, with 20 consecutive frames used for detection.

When drowsiness is detected, the system generates an audio alert using the pyttsx3 text-to-speech library to notify the driver.

### B. Obstacle Detection

The obstacle detection module identifies potential obstacles in front of the vehicle using camera-based visual analysis.

It monitors detected objects and provides visual indicators according to their proximity.

- **Red Indicator:** Represents a nearby obstacle that requires immediate attention.
- **Yellow Indicator:** Represents an obstacle detected at a greater distance, indicating caution.

This module helps the driver remain aware of potential hazards and supports safer driving decisions.

### C. Audio Alert System

The system uses the pyttsx3 library to generate voice-based alerts when potentially unsafe driving conditions are identified.

Audio notifications help bring the driver's attention to drowsiness or nearby obstacles without requiring them to continuously observe the dashboard.

### D. Trip Monitoring

The trip monitoring module provides an overview of the current journey.

It includes:

- Trip initiation and monitoring.
- Destination information.
- Route overview using an open-source mapping API.
- Safety status during the journey.
- Visual indicators for detected drowsiness and obstacles.

This functionality helps users understand trip conditions and monitor safety-related events.

### E. Safety Analytics Dashboard

The web-based dashboard provides a centralized interface for viewing vehicle safety information and trip-related analytics.

It includes:

- Safety performance indicators.
- Trip-related safety information.
- Drowsiness and obstacle monitoring status.
- Visual representation of safety-related data.
- An overview of vehicle monitoring activities.

The safety rate is designed to reflect detected risk conditions, helping users understand how driving safety changes during a trip.

### F. Fleet Management

The fleet management module allows users to add and manage vehicle information through the dashboard.

It provides a centralized view of registered vehicles and supports vehicle-level management within the application.

### G. User Interface and Customization

The dashboard provides an interactive interface with:

- Dark and light theme support.
- Configurable monitoring options.
- Interactive dashboard components.
- Vehicle and trip information.
- Visual safety indicators.

## 5. Technologies and Tools Used

| Technology | Purpose |
|---|---|
| Python | Core application development |
| OpenCV | Image processing and camera-based monitoring |
| Dlib | Facial landmark detection |
| NumPy | Numerical computations |
| SciPy | Mathematical and scientific computations |
| pyttsx3 | Voice-based safety alerts |
| HTML | Dashboard structure |
| CSS | Dashboard styling |
| JavaScript | Dashboard interactions |
| Machine Learning | Intelligent detection and analysis |
| Open-source Mapping API | Trip route visualization |

## 6. Working Methodology

The application follows a combination of camera-based monitoring, image processing, detection logic, alert generation, and dashboard visualization.

**Step 1: Camera Input**

The camera captures the driver's facial information and visual information about the road.

**Step 2: Facial Landmark Detection**

OpenCV processes the camera frames, while Dlib identifies 68 facial landmark points to locate the driver's eyes.

**Step 3: EAR Calculation**

The system calculates the Eye Aspect Ratio to determine the driver's eye state.

**Step 4: Drowsiness Identification**

The system checks whether the EAR remains below the configured threshold for the specified number of consecutive frames.

**Step 5: Obstacle Monitoring**

The obstacle detection module analyzes the visual input to identify potential obstacles and determine their proximity.

**Step 6: Alert Generation**

When an unsafe condition is identified, the system provides appropriate audio and visual alerts.

**Step 7: Dashboard Visualization**

Trip information, safety indicators, and analytics are displayed through the web dashboard.

## 7. Project Outcome

The project demonstrates how computer vision and machine learning techniques can be applied to vehicle safety applications.

It brings together driver drowsiness detection, obstacle monitoring, alert generation, trip monitoring, and safety analytics in a single application.

The system provides an integrated approach to driver safety by helping identify potentially dangerous situations and notifying the driver through appropriate alerts.

## 8. Future Enhancements

- Improve detection accuracy under different lighting conditions.
- Integrate more advanced object detection models.
- Enhance obstacle distance estimation.
- Introduce additional trip safety reports and analytics.
- Improve dashboard reporting and visualization.
- Extend fleet management capabilities.

## 9. Conclusion

The Smart Vehicle System is an attempt to make driving safer through intelligent monitoring and early warning mechanisms. By combining facial landmark analysis, computer vision, obstacle detection, audio alerts, and web-based analytics, the application provides a practical demonstration of AI-based safety technology.

The project also demonstrates the integration of Python-based computer vision modules with an interactive web dashboard to develop a complete application addressing a real-world problem.

---

**Project Domain:** Artificial Intelligence, Machine Learning, Computer Vision, Automotive Safety

**Project Type:** Academic / Software Development Project
