# Mid-Term Project Write-Up: 3D Sensor Fusion
## Section 1 : Compute Lidar Point-Cloud from Range Image
###### ID S1-EX1: Visualize range image channels
![range_image_ID_S1_EX1](https://user-images.githubusercontent.com/109758200/184568640-d51d913c-7792-410a-b36c-0c66a1c6165c.png)

###### ID S1-EX2: Visualize lidar point-cloud 

Below showing Lidar pointclouds for 7 frames:

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
###### ID_S2_EX1: Convert sensor coordinates to BEV-map coordinates
![LidarBEV_ID_S2_EX1](https://user-images.githubusercontent.com/109758200/184567784-5158f535-a20d-4f64-8bb9-a12cd265134f.JPG)

###### ID_S2_EX2: Compute intensity layer of the BEV map
![ImageIntensity_ID_S2_EX2](https://user-images.githubusercontent.com/109758200/184568090-98da3f41-802d-4173-8b21-f1f8af39fd61.JPG)


###### ID_S2_EX3: Compute height layer of the BEV map
![ImageHeight_ID_S2_EX3](https://user-images.githubusercontent.com/109758200/184568109-1659599f-bdc2-4efa-8eee-37b8f520812d.JPG)




## Section 3 : Model-based Object Detection in BEV Image
###### ID_S3_EX1: Add a second model from a GitHub repo

Frame 50:
![3DBoundingBox_and_Image_Frame50_ID_S3_EX1](https://user-images.githubusercontent.com/109758200/184568151-6753cfab-af24-46a7-8ed6-489badbf6ca2.JPG)
Frame 51:
![3DBoundingBox_and_Image_Frame51_ID_S3_EX1](https://user-images.githubusercontent.com/109758200/184568179-10b26828-02b2-4d23-b453-4f8bb33efbf5.JPG)


###### ID_S3_EX2: Extract 3D bounding boxes from model response
Frame 50:
![3DBoundingBox_and_Image_Frame50_ID_S3_EX2](https://user-images.githubusercontent.com/109758200/184568198-94b949b3-8056-4045-a635-636510ee6b2c.JPG)
Frame 51:
![3DBoundingBox_and_Image_Frame51_ID_S3_EX2](https://user-images.githubusercontent.com/109758200/184568222-afd76a12-41f6-4b4b-bb02-7f19a5d63eaf.JPG)

## Section 4 : Performance Evaluation for Object Detection
###### ID_S4_EX1: Compute intersection-over-union between labels and detections
![GraphingPerformanceMetrics_ID_S4_EX1](https://user-images.githubusercontent.com/109758200/184568734-129cdf4d-c214-4ca1-94ad-5b7885e7d90a.png)

###### ID_S4_EX2: Compute false-negatives and false-positives
###### ID_S4_EX3: Compute precision and recall
![GraphingPerformanceMetrics_ID_S4_EX3](https://user-images.githubusercontent.com/109758200/184568811-b2f5ba81-6054-4922-a660-900815699218.png)
