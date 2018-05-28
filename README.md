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

 ### 2.2 Using 
