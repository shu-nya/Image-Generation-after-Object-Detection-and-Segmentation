# Image-Generation-after-Object-Detection-and-Segmentation


### Objective

This project is focused on creating a pipeline that performs image inpainting and outpainting with Generative AI using an input image and a few text prompts.


### Data

The images on which the pipeline works have been taken from Kaggle. One can also use images of their own choice.


### Steps performed

1. Grounding DINO has been used to interpret our text input prompt and perform object detection by predicting bounding boxes for the input labels.

Grounding DINO sets a new standard in the world of object detection by offering a highly adaptable and flexible zero-shot detection model. The model's ability to identify objects outside its training set and understand both language and visual content allows it to excel in various real-world tasks.

2. SAM has been used to segment the masks within the bounding box predictions.

SAM is a prompt-able segmentation system with results that are simply stunning. It excels in zero-shot generalization to unfamiliar objects and images without the need for additional training. It’s also considered the first foundational model for computer vision. SAM has been trained on a massive dataset of 11 million images with 1.1 billion segmentation masks, which Meta has also released publicly.

The Segment Anything Model requires no additional training, so all we need to do is provide a prompt that tells the model what to segment in a given input image.

3. Finally, the masks generated from SAM have been used to isolate regions of the image for either inpainting or outpainting with Stable Diffusion.

Stable diffusion is a text-to-image model of Deep Learning. It makes it possible to create images that are conditioned by textual descriptions. Hence, it allows people to be creative by converting their thoughts into real images.


### Conclusion

A pipeline has been created that detects the objects in the image, segments the image, and thereafter, based on the prompts given by the user generates a new image by making modifications in the different segments of the image.

Here, are a few of the generated images.


![img gen bg waterfall](https://github.com/shu-nya/Image-Generation-after-Object-Detection-and-Segmentation/assets/115604932/8562e9af-9fd1-43ff-a94d-c9848c53bc1c)

![img gen bg casino](https://github.com/shu-nya/Image-Generation-after-Object-Detection-and-Segmentation/assets/115604932/4b1a2f0e-f435-408d-b61f-3b4bbe70498b)

![img gen bull dog](https://github.com/shu-nya/Image-Generation-after-Object-Detection-and-Segmentation/assets/115604932/ec1bd37a-1e55-4991-a0d0-e5b560765aa7)

![img gen mask](https://github.com/shu-nya/Image-Generation-after-Object-Detection-and-Segmentation/assets/115604932/b289867a-bbf5-4499-8bcc-ba8847815f92)
