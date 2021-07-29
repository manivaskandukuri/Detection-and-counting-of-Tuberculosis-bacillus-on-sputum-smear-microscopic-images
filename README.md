# Detection-and-counting-of-Tuberculosis-bacillus-on-sputum-smear-microscopic-images
As a summer intern trainee at Siemens Healthineers, Bangalore, reviewed existing literature and developed an automated technique to diagnose the level of infection of Tuberculosis (TB) disease based on the count of TB bacilli on sputum smear microscopic images. During this project, worked on the following activities to detect and count the number of TB bacilli for a given test image:

(a) Image preprocessing (image segmentation and postprocessing)
(b) Extraction of geometrical features and formation of data matrix
(c) Outlier rejection and data balancing
(d) Classification using Random Forest classifier and identification of single and overlapped bacilli
(e) Counting the number of bacilli in each overlapped bacillus by separating it based on concave points and fitting ellipse to each segment
(f) Calculate the final count of all single bacilli.

# About the project:
Among the several methods of Tuberculosis (TB) diagnosis, sputum smear microscopy test is a non-invasive and economical one and is therefore, mostly preferred. In this test, the level of TB infection is identified by counting the number of TB bacilli count on the microscopic image. This counting process is manually performed by an expert technician. But manual identification and counting of bacilli is a very time consuming and labor-intensive task. Also, the sensitivity of TB detection relies on the experience of technician. To address these shortcomings, an automated method of detection and counting of TB bacilli is required, which will not only increase the accuracy but also reduces the time of diagnosis.

The overall scope of this project is to identify the potential bacilli object, classify it into either of the 3 classes i.e., single bacillus, bacilli cluster and artifacts, count the number of single bacilli in each bacilli cluster and hence calculate the total number of single bacilli on a given image.

Using the ground truth information available on the microscopic images, annotation is performed on each image and corresponding annotation file is generated for each image.
On the given input image, color space-based segmentation is applied to separate the potential TB objects from the background. Then post processing is performed on the segmented image to remove the smaller size artifacts. From the post processed image, contours are extracted from each object on the image and geometric features (like Relative convex area, Eccentricity, Roughness etc.,) are calculated for each contour. Using the ground truth information in the annotation file, each contour is assigned a class label. Similar procedure is applied for all the images and a final labelled data matrix is created using the afore-mentioned features and class details of all the images. Random forest classifier is developed by training it using the labelled data matrix. For a given test image, each potential TB object is classified into one of the 3 classes (i.e., single bacillus, bacilli cluster and artifacts) using Random forest classifier. Concave points are identified on the bacilli cluster and the same are used to count the number of single bacilli in each bacilli cluster. Hence, an overall count of single bacilli is obtained for a given test image. 
