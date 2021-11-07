# Objective of the Task
 - The objective of this task is to predict keypoint positions on face images. This can be used as a building block in several applications, such as:
    - tracking faces in images and video
    - analysing facial expressions
    - detecting dysmorphic facial signs for medical diagnosis
    - biometrics / face recognition

# Dataset Description
 - Dataset is from a kaggle competition - Facial Keypoints Detection
     - The dataset is provided by [ Dr. Yoshua Bengio](https://yoshuabengio.org/) from the University of Montreal.
     - The dataset contains images of faces and their corresponding keypoints
     - The keypoints are the points on the face that are used to detect the face
     - The dataset is split into training and testing sets
     - [click the link to see the competition](https://www.kaggle.com/c/facial-keypoints-detection)

 - Data Description (from kaggle)
   - Each predicted keypoint is specified by an (x,y) real-valued pair in the space of pixel indices. There are 15 keypoints, which represent the following elements of the face:
   - left_eye_center, right_eye_center, left_eye_inner_corner, left_eye_outer_corner, right_eye_inner_corner, right_eye_outer_corner, left_eyebrow_inner_end, left_eyebrow_outer_end, right_eyebrow_inner_end, right_eyebrow_outer_end, nose_tip, mouth_left_corner, mouth_right_corner, mouth_center_top_lip, mouth_center_bottom_lip
   - Left and right here refers to the point of view of the subject.
   - In some examples, some of the target keypoint positions are misssing (encoded as missing entries in the csv, i.e., with nothing between two commas).
   - The input image is given in the last field of the data files, and consists of a list of pixels (ordered by row), as integers in (0,255). The images are 96x96 pixels.

 - Data files (from kaggle)
    - training.csv: list of training 7049 images. Each row contains the (x,y) coordinates for 15 keypoints, and image data as row-ordered list of pixels.
    - test.csv: list of 1783 test images. Each row contains ImageId and image data as row-ordered list of pixels
    - submissionFileFormat.csv: list of 27124 keypoints to predict. Each row contains a RowId, ImageId, FeatureName, Location. FeatureName are "left_eye_center_x," "right_eyebrow_outer_end_y," etc. Location is what you need to predict.
