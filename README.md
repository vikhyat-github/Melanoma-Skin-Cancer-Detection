# Melanoma-Skin-Cancer-Detection
This is a project about melanoma detection methods using convolutional neural networks.

> Melanoma is a deadly type of skin cancer whose pri- mary cause is Ultraviolet light (UV) exposure and it spreads quickly. As a result, it is the worst skin cancer and the lead- ing cause of mortality. When a patient is diagnosed, the classification of cancer stages is a time-consuming and te- dious task. Cancer diagnosis at the time of surgical ther- apy is primarily determined by the cancer’s stage or tumour thickness.We broadly classify the melanoma into two cate- gories namely benign melanoma and malignant melanoma. We aim to propose a model which can successfully classify the cancer stage backed by strong accuracy.
Benign is well-differentiated and has abnormally slow growing skin cancer which does not invade surrounding tis- sue or spread to other parts of the body. cells are not can- cerous and it is comparatively easy to remove with surgery. Whereas,Malignant is poorly-differentiated and is abnor- mally fast growing skin cancer that can invade and destroy nearby tissues and can also spread to other body parts. cells are cancerous and it is difficult to remove them so the pa- tient is treated with chemotherapy and radiation therapy.

<img width="1083" alt="Screenshot 2022-06-28 at 11 08 59 PM" src="https://user-images.githubusercontent.com/55956769/176247435-47e3f2f3-1821-4009-9a9a-f2d12e977e17.png">

# Feature Extraction
> We have preformed 4 pre-processing layers to our data (dull razor, median filter, Otsu and Chanvese algorithm) which removes hairs, data-segmentation and all the other noises from our images, after which we get our final images that we use for training and testing our model. we are ex- tracting features like Asymmetry index - the average of the difference between lesion image and its horizontal flip and lesion image and its vertical flip and the total lesion area , Eccentricity-The ratio of the distances of a point on the shape from the focus, Border Irregularity - Border irregu- larity the compact index - P2/4π*A , Diameter-Diameter of the Circle with same Area, Corelation- measures the joint probability occurrence of the specified pixel pairs, Ho- mogeniety - measures the closeness of the distribution of elements in the GLCM with respect to the GLCM diago- nal, Energy-It is computed as the square root of the sum of squared elements in the GLCM, Contrast- It measures the local variations in the GLCM
These features are then trained on different models.


## Confusion Matrix and loss curve for best performing model
<img width="419" alt="Screenshot 2022-06-28 at 10 55 34 PM" src="https://user-images.githubusercontent.com/55956769/176244957-c501a11e-9890-472c-9e63-95cefdb8a161.png">

> The binary cross entropy is used as the loss function, it calculates the loss on the basis of how close or far we are from the actual value. The Optimizer is used as Adam with learning rate to be 0.01.The Adam optimizer has the best accuracy in enhancing the CNN ability in classification and segmentation. CNN was applied on two different feature set. The set with 7 features gave test accuracy of 77.56 while running the network on 80 extracted features gave an accuracy of 97.13

## Metrics
<img width="419" alt="Screenshot 2022-06-28 at 10 55 49 PM" src="https://user-images.githubusercontent.com/55956769/176245003-e5ca5eab-7802-4644-8fc4-4350b76d6b27.png">

## References
[1] Patil & Bellary (2020) . Machine learning approach in melanoma cancer stage detection, Journal of King Saud University

[2] Pascal Getreuer, Image Processing On Line (2012) Chan-Vese Segmentation, scikit-image: Image process- ing in Python (2014)

[3] Murzova & Seth (2020) Otsu’s Thresholding with OpenCV

[4] Jason Brownlee (2019) A Gentle Introduction to Pool- ing Layers for Convolutional Neural Networks
