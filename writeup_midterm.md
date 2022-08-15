# Mid-Term Project Write-Up: 3D Sensor Fusion
## Section 1 : Compute Lidar Point-Cloud from Range Image
#### ID S1-EX1: Visualize range image channels
![range_image_ID_S1_EX1](https://user-images.githubusercontent.com/109758200/184568640-d51d913c-7792-410a-b36c-0c66a1c6165c.png)

#### ID S1-EX2: Visualize lidar point-cloud 

Below Lidar pointclouds are visualized for 7 frames. The provided results show that bumpers (rear-bumber and front-bumper), license plate, windshields, sides of vehicles are stable features.

Frame 1:
![LidarPCL1_ID_S1_EX2](https://user-images.githubusercontent.com/109758200/184567799-ee3fd397-bb65-410c-809a-953ee5dcad7a.JPG)
Frame 2:
![LidarPCL2_ID_S1_EX2](https://user-images.githubusercontent.com/109758200/184567840-162e5acb-7976-4b93-97b1-cd88a3866d25.JPG)
Frame 3:
![LidarPCL3_ID_S1_EX2](https://user-images.githubusercontent.com/109758200/184567872-2a76d321-1409-4334-8979-b1264980a5de.JPG)
Frame 4:
![LidarPCL4_ID_S1_EX2](https://user-images.githubusercontent.com/109758200/184567874-09d5761f-f49b-4c98-b048-0d6934119ea9.JPG)
Frame 5:
![LidarPCL5_ID_S1_EX2](https://user-images.githubusercontent.com/109758200/184567883-4bb80dc5-1b46-41c6-aa29-6fee872c4236.JPG)
Frame 6:
![LidarPCL6_ID_S1_EX2](https://user-images.githubusercontent.com/109758200/184567889-b581be47-cc8c-4f6d-a1b6-db62722e5e88.JPG)
Frame 7:
![LidarPCL7_ID_S1_EX2](https://user-images.githubusercontent.com/109758200/184567577-812af084-793e-433d-83b4-577b1e96d385.JPG)



## Section 2 : Create Birds-Eye View from Lidar PCL
#### ID_S2_EX1: Convert sensor coordinates to BEV-map coordinates
![LidarBEV_ID_S2_EX1](https://user-images.githubusercontent.com/109758200/184567784-5158f535-a20d-4f64-8bb9-a12cd265134f.JPG)

#### ID_S2_EX2: Compute intensity layer of the BEV map

Image Intensity is shown below:

![ImageIntensity_ID_S2_EX2](https://user-images.githubusercontent.com/109758200/184570237-6f569cd1-d289-44ba-b6fd-b40e5112e3ef.JPG)


#### ID_S2_EX3: Compute height layer of the BEV map

Image Height is shown below:

![ImageHeight_ID_S2_EX3](https://user-images.githubusercontent.com/109758200/184570258-094966de-b6eb-40b1-ad94-00557650a6e1.JPG)


## Section 3 : Model-based Object Detection in BEV Image
#### ID_S3_EX1: Add a second model from a GitHub repo
Below, `detections` computed for frame 51 and 51 are shown:

![image](https://user-images.githubusercontent.com/109758200/184576097-42db58e0-eb78-49b7-9a25-a0be272ba0ce.png)

#### ID_S3_EX2: Extract 3D bounding boxes from model response

Frame 50:

![3DBoundingBox_and_Image_Frame50_ID_S3_EX2](https://user-images.githubusercontent.com/109758200/184568198-94b949b3-8056-4045-a635-636510ee6b2c.JPG)

Frame 51:

![3DBoundingBox_and_Image_Frame51_ID_S3_EX2](https://user-images.githubusercontent.com/109758200/184568222-afd76a12-41f6-4b4b-bb02-7f19a5d63eaf.JPG)

## Section 4 : Performance Evaluation for Object Detection
#### ID_S4_EX1: Compute intersection-over-union between labels and detections

Below, `ious` and `center_devs` for frame 51 is shown:

![Ious_centerdevs_F51_ID_S4_EX1](https://user-images.githubusercontent.com/109758200/184574121-1acf2ec0-e540-4ee9-818c-17cfc00d4e97.png)

#### ID_S4_EX2: Compute false-negatives and false-positives

Below, `det_performance` for frame 51 is shown:

![det_performance_F51_ID_S4_EX2](https://user-images.githubusercontent.com/109758200/184574512-f5492677-345e-4815-8536-ffd5cc7a1a69.png)

#### ID_S4_EX3: Compute precision and recall
For frames 50 to 150, precision and recall is calculated with ```configs_det.use_labels_as_objects=False``` to use model-based detection as objects. The results are shown below:

![FP_FN_ID_S4_EX3](https://user-images.githubusercontent.com/109758200/184576286-70e9ec10-4021-4396-8b1e-59205e67f9e9.png)


![GraphingPerformanceMetrics_ID_S4_EX3_mdlbased](https://user-images.githubusercontent.com/109758200/184575635-27fbd8dc-d3d0-4ab3-81f7-308c594fbfea.png)

Now, to verify our code, we set the following code: ```configs_det.use_labels_as_objects=True``` to use groundtruth labels as objects. This should result in precision and recall values equal to 1: 

![PrecRecall_ID_S4_EX3](https://user-images.githubusercontent.com/109758200/184572909-f361a006-9ec7-41d1-9845-62e8451339ec.png)

![GraphingPerformanceMetrics_ID_S4_EX3_new](https://user-images.githubusercontent.com/109758200/184572917-e434e1dc-cd94-4b2a-8c81-e53c0148a7a3.png)

