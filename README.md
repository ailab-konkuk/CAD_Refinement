# CAD_Refinement

<img src="./images/system_architecture.png" width="800">

Enhanced Pose Detection of Nearby Vehicles Using LiDAR and Prior Shape for Autonomous Driving

The code will be uploaded after the review process!

## Purpose
Enhancing LiADR-based 3D bounding box detection with prior car shape model 

## Method

1. Downsample vehicle prior model into **Surfel Model**
<img src="./images/shape_to_surfel.png" width="500">
<!-- <img src="./images/various_voxel_size.png" width="800"> -->


2. 4-DoF Point-to-Surfel Registration.
<img src="./images/refinement_process.png" width="500">

## Demo
* Stop Scenario Comparision
<img src="./images/stop_scenario_comparison.gif" width="800">

## Run Algorithm
1. Detection only
```
roslaunch box_point_generator box_point_generator.launch
roslaunch cad_registration cad_registration.launch
```

2. Run Tracking
```
roslaunch object_tracking ca_xy_kf_gnn_cost_matrix_global_tracker.launch
```

# Evaluation


* Evaluation Setup
<img src="./images/evaluation_setup.png" width="800">

* Scenario Example
<img src="./images/4_scenario.gif" width="800">

## Scenario Bag file

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

1. Need GNSS Topic from target vehicle (Existed in bag files)
* /novatel/oem7/inspvax

2. Ego detection topoic type should be "**autoku_types::DetectsObjects**"
* topic_name/ego_detection_topic_name



### Run Evaluation Tool
1. 
```
roslaunch detection_evaluation detection_evaluation.launch
```
2. rviz file in /rviz/autoku_evaluation.rviz

3. Type scene number when "Enter index of scene to visualize ('q' to quit)" pop up