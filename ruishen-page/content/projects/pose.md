{
  "title": "Mobile C-arm Pose Estimation",
  "date": "2018-05-01",
  "image": "/img/pose-net.png",
  "description": "This project was to estimate the 6 degrees-of-freedom pose of the mobile C-arm imaging device based on a single image. The motivation was to determine the best device position within limited X-ray shots in order to reduce unnecessary radiation exposure administered by the system. My work involved investigating different design markers by which to encode the device pose, and I decoding the pose through segmentation and registration methods. In addition, I implemented an end-to-end learning scheme to train a deep neural network based on the whole image information, using tens of thousands synthetic X-ray data I generated.",
  "tags": ["Python","Tensorflow","OpenCV","Registration","Mobile C-arm","X-ray","PoseNet","Homoscedasticity Uncertainty"],
  "fact": "",
  "featured":true
}
This project's object was to estimate the 6 degrees-of-freedom pose of the mobile C-arm imaging device based on a single image. The motivation of this work was to determine the best device position within limited X-ray shots in order to reduce unnecessary radiation exposure administered by the system. My work involved investigating different design markers by which to encode the device pose, and I decoding the pose through segmentation and registration methods. In addition, I developed an end-to-end learning scheme to train a deep neural network based on the whole image information, using tens of thousands synthetic X-ray data I generated. Also, I applied homoscedasticity uncertainty in the neural network to estimate the error balancing ratio in order to reduce hyperparameter tuning.