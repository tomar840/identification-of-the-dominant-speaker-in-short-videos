# identification-of-the-dominant-speaker-in-short-videos
Here in this project, we have tried to find out the dominant speaker in YouTube videos. Videos from YouTube has to be classified into 7 categories i.e. 
6 personalities and 1 class as noise (frames when speaker is absent). 6 personalities are -
  * [Sandeep Maheshwari](https://www.youtube.com/user/SandeepSeminars)
  * [Raman Flute](https://www.youtube.com/user/fluteraman)
  * [Sadhguru](https://www.youtube.com/user/sadhguru)
  * [Saurabh Pant](https://www.youtube.com/user/PantOnFireComedy)
  * [Atul Khatri](https://www.youtube.com/channel/UCoAkOJtcToS0piLQMO-W4uw)
  * [Shailendra Kumar](https://www.youtube.com/channel/UCc6tYtmPd-1aEtr5TCu3a8Q)
## 1. Data
  Videos from YouTube are taken of these 6 personalities in 720p quality. Frames are extracted at 1 fps from these videos using ffmpeg.
 
## 2. Approaches 
  ### 2.1 Using face embeddings
Since in every video has a unique speaker, so first we try to solve this problem using face recognition. For finding face embeddings we have 
used [OpenFace Library](https://cmusatyalab.github.io/openface/). 

 ### 2.2 Using Spatial Models
 Since the problem is basically object detection, so we haved tried to use transfer learning for CNN pre-trained on ImageNet. 
 We did two types of fine tuning on CNN -
  #### 2.2.1 Tuning of all layers of CNN.
  Weights of pre-trained CNN has been used for initialization and parameters of all the layers has been updated.
  
  #### 2.2 Tuning of only final layer
  Only the parameters of last layer of CNN has been updated while the rest of the layers has been freezed. 
  
  
## 3. Data Augmentation
 We have used data augmentation for avoiding the over-fitting of the models. We have randomly cropped frame, flip it horizontal and cropped it. We have included faces of these personalities to avoid CNN remebering the background of the frames. These faces were extracted from the [OpenFace Library](https://cmusatyalab.github.io/openface/). 
