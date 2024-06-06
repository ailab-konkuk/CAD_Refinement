# CAD_Refinement
Enhanced Pose Detection of Nearby Vehicles Using LiDAR and Prior Shape for Autonomous Driving

The code will be uploaded after the review process!

## Purpose
Enhancing LiADR-based 3D bounding box detection with prior car shape model 


## Demo
* Stop Scenario Comparision
<img src="./images/stop_scenario_comparison.gif" width="800">



# Evaluation Tool
## Scenario Bag file

* Evaluation Setup
<img src="./images/evaluation_setup.png" width="800">

* Scenario Example
<img src="./images/4_scenario.gif" width="800">


1. Stop Scenario
    1. Ego: 
    2. Target 1: 
    3. Target 2:
2. Slow Scenario
    1. Ego: 
    2. Target 1: 
    3. Target 2:
3. Fast Scenario 1
    1. Ego: 
    2. Target 1: 
    3. Target 2:
4. Fast Scenario 2
    1. Ego: 
    2. Target 1: 
    3. Target 2:

### Data Preparation
Fix /config/system.yaml

1. Needed topic from target_?_path:
* /novatel/oem7/inspvax

2. Ego detection topoic type should be "autoku_types::DetectsObjects"
* topic_name/ego_detection_topic_name



### How to Use
1. 
```
roslaunch detection_evaluation detection_evaluation.launch
```
2. rviz file in /rviz/autoku_evaluation.rviz

3. Type scene number when "Enter index of scene to visualize ('q' to quit)" pop up