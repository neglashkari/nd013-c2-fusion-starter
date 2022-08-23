# Final Project: Sensor Fusion and Object Tracking

## Step 1: Implement an extended Kalman filter.

In this step, an EKF is implemented for a Lidar measurement. This is done via two steps: 1) predict and 2) update for states x and error covriance P. Codes are captured in `filter.py`.

A snapshot of obtained result is shown below for a single target tracking via Lidar mesurements:
![Step1_EKF](https://user-images.githubusercontent.com/109758200/186170506-ca400a4a-aaeb-45e8-92b0-092da54e63e3.PNG)

Root Mean Square Error (RMSE) of Lidar tracking is shown below:
![Step1_RMSE](https://user-images.githubusercontent.com/109758200/186170522-63bddd8a-b293-4bc2-a461-07d82d05ad87.PNG)

The mean of RMSE is 0.32 (as shown in the picture above), i.e. smaller than 0.35 mentioned in `Project Instruction Step 1`.

## Step 2: Implement track management including track state and track score, track initialization and deletion.
In this step, we perform track management and the code is implemented in `trackmanagement.py`. In this step, the followings were implemented:
- **state initialization:** new tracks were instialized (states x and error covariance P) with unassigned Lidar measurements;
- **track score:** calculating score based on measurements corrolation;
- **track state:** assigning a track state (initialized, tentative, confirmed) based on calculated track score;
- **track deletion:** removing the track if its score is below a threshold or error covariance P is too large.
![Step2_tracking](https://user-images.githubusercontent.com/109758200/186170561-0b78961d-2d76-43bd-b900-b9fbf21c9809.PNG)
![Step2_RMSE](https://user-images.githubusercontent.com/109758200/186170576-55ba03e4-917a-4664-afa7-852a56f4b22e.PNG)

## Step 3: Implement single nearest neighbour data association and gating.
![Step3_association_2](https://user-images.githubusercontent.com/109758200/186170687-46083032-6b3b-4302-a0fa-df9c6ebd6003.PNG)
![Step3_association_3](https://user-images.githubusercontent.com/109758200/186170700-599948ac-8bb3-44f8-8950-8a8f505e0c48.PNG)
![Step3_association_5](https://user-images.githubusercontent.com/109758200/186170803-a039d69a-c3ca-4628-a24f-6d8d99cca49c.PNG)
![Step3_association_6](https://user-images.githubusercontent.com/109758200/186170814-d6307ad4-0219-4845-a32c-936a194f3b98.PNG)
![Step3_association_8](https://user-images.githubusercontent.com/109758200/186170851-782df277-6e99-48a7-a35d-603a360c513e.PNG)
![Step3_RMSE](https://user-images.githubusercontent.com/109758200/186170859-ca03bc11-b776-4b20-ab4f-f1b00554397c.PNG)


## Step 4: Apply sensor fusion by implementing the nonlinear camera measurement model and a sensor visibility check.
![Step4_meas_3](https://user-images.githubusercontent.com/109758200/186170962-e853ace1-21bf-43ad-aae6-05b46bfd2f42.PNG)
![Step4_meas_4](https://user-images.githubusercontent.com/109758200/186170997-3b8f3ab2-7c47-4c11-8d00-40577fb49228.PNG)
![Step4_RMSE](https://user-images.githubusercontent.com/109758200/186171072-77c805ad-20c2-4c79-8141-e277d12d2652.PNG)


#### Do you see any benefits in camera-lidar fusion compared to lidar-only tracking (in theory and in your concrete results)?
#### Which challenges will a sensor fusion system face in real-life scenarios?
#### Did you see any of these challenges in the project?
#### Can you think of ways to improve your tracking results in the future?
