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

The overall scope of this project is to annotate the train images, apply image processing techniques to identify the potential bacilli objects, classify the objects into either of the 3 classes (i.e., single bacillus, bacilli cluster and artifacts), count the number of single bacilli in each bacilli cluster and hence calculate the total number of single bacilli on a given image.

Using the ground truth information available on the microscopic images, annotation is performed on each image and a corresponding annotation file is generated for each image.
Image processing operations, i.e., image segmentation and image postprocessing are performed on the microscopic images to separate the potential TB objects from the background. Since, bacilli objects belonging to different classes can be distinguished based on their geometrical features (like Relative convex area, Eccentricity, Roughness etc.,), these features can be used as input to the Machine algorithms to classify the bacilli. For each object in the postprocessed image, geometric features are extracted and class label is assigned based on the ground truth information available in the annotation file. Similar procedure is applied to all the images and a final labelled data matrix is created using the afore-mentioned features and class labels. Random forest classifier is trained using the labelled data matrix. For a given test image, each potential TB object is classified into one of the 3 classes (i.e., single bacillus, bacilli cluster and artifacts) using the random forest classifier. Concave points are detected on the bacilli cluster and the same are used to count the number of single bacilli in each bacilli cluster. Finally, an overall count of single bacilli is obtained for a given test image

[Project_Report.pdf](https://github.com/manivaskandukuri/Detection-and-counting-of-Tuberculosis-bacillus-on-sputum-smear-microscopic-images/files/6903189/Project_Report.pdf)

