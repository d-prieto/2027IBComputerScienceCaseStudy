# Definitions

Here you find almost all the concepts that you need. For context definitions you will require to check the [other markdown document](https://github.com/d-prieto/2027IBComputerScienceCaseStudy/blob/main/Context%20definitions.md).

# Standard level and higher level technical part

## Text-to-image generation

Text-to-image generation is an AI process that turns typed words into custom pictures. It uses machine learning models to understand the meaning of the text prompt and generate an image based on the user’s description, including elements such as objects, people, environments, colours, and artistic styles.

## Conditional image generation

Conditional image generators are models designed to synthesize images under explicit control provided by conditioning inputs, such as class labels, attributes, textual descriptions, example images, spatial maps, or multimodal cues.

The process of this is by providing an input signal to the AI model and it converts it into a mathematical guide and uses it to shape random visual noise into a matching picture.

(https://www.emergentmind.com/topics/conditional-image-generators)

## Segmentation map 

![](https://www.researchgate.net/profile/Sagi-Eppel/publication/339698501/figure/fig1/AS:865545939320832@1583373641463/Exclusive-instance-segmentation-map-from-the-Vector-LabPics-dataset-The-segmentation-is.png)
source: https://chemrxiv.org/doi/full/10.26434/chemrxiv.11930004.v3

## Class labels

Discrete categorical tags that guide generative models to create images belonging to a specific category. So, instead of generating random images, the model can receive an integer or one-hot encoded class label (like "dog", "cat") alongside random noise. The label provides the required category features for the generated output to match. 

## Image-to-image translation
It is a sub-field of computer vision and deep learning where the goal is to map an input image from one domain and an output image in another domain. In simpler words it maps a pattern to another, such as a a winter landscape to a summer landscape.


<img width="1400" height="673" alt="0_Udvw6tGu40iDEkuH" src="https://github.com/user-attachments/assets/30e3141f-8862-40d9-8d91-9e215255c218" />
<img width="431" height="464" alt="images" src="https://github.com/user-attachments/assets/b55938e7-4903-4624-a92b-9c72effadff4" />





## Unconditional image generation

It is an AI image generation of random samples of its training data without any guidance, prompts or context. It is used in synthetic data creation, as it does not violate any privacy policies, as it generates faces of people that don't exist. It starts with a seed of a random noise image and applies patterns from the learnt data, to create a realistic image.

![](https://miro.medium.com/v2/resize:fit:720/format:webp/1*W_TqD_l6OhXZGVpT0Y91vQ.png)

Unconditional Image Generation. (2023, August 3). huggingface.co. https://huggingface.co/tasks/unconditional-image-generation

Michael ZHANG. (2023, February 15). Diffusion Models : Unconditional&Conditional Image Generation. Medium. https://medium.com/@myschang/diffusion-models-unconditional-conditional-image-generation-e7ced52b09b5

## Diffusion model 

### Noise injection 
Noise injection is a technique that introduces controlled randomness into training data to improve generalization. It does so by utilizing tools like Gaussian Noise which forces models to learn patterns rather than focusing on individual pixels. This allows for the models to be more used to realistic images which helps it function significantly better in the real world. 

<img width="1048" height="497" alt="image" src="https://github.com/user-attachments/assets/b56d97f1-a1c6-4e45-aacd-e06db8316f03" />


Understanding noise injection in gans. (n.d.). http://proceedings.mlr.press/v139/feng21g/feng21g.pdf 

### Denoising 
Denoising is a computational process that eliminates noise from a picture. Noise can be present on a picture due to: transmission errors and sensor limitations. Types of denoising processes include: Gaussian Noise, Salt and pepper noise, Poisson noise and speckle noise. The need for multiple processes stems from the fact that different noises require different approaches. 

Kumar, P. (2025, May 9). What Is Image Denoising & What Are Its Methods? E-Con Systems. https://www.e-consystems.com/blog/camera/technology/what-is-image-denoising-what-are-its-methods/
‌

### Convolutional neural network (CNN)
A convolutional neural network is a type of neural network that learns via kernel optimization. This type of neural network can be used to process and make predictions in various types of data such as: text, images and audio. This is the main type of neural network used in order to train for image processing. They also consist of an input layer, hidden layers and an output layer. The hidden layers include one or more layers that perform convolutions.
<img width="960" height="720" alt="image" src="https://github.com/user-attachments/assets/be88cd2b-a043-4d6b-9b8c-07dc7c7377d6" />

Taken from wikipedia. https://en.wikipedia.org/wiki/Convolutional_neural_network

### Denoising diffusion probabilistic model (DDPM)

Denoising diffusion probabilistic models are a class of AI models that create new data by reversing a noise adding process. This works by slowly denoising an image, as it has been trained to predict and remove noise step-by-step to recover a clean image. However, it does not return the de-noised image, instead it denoises an image to create a new image that might be completely different.

![](https://miro.medium.com/v2/resize:fit:1400/1*yvClU5LgylulNWLPNpOCfA.png)
![](https://www.siam.org/media/agxdzywa/figure1.jpg)

# Higher level only technical part 

## Generative adversarial network (GAN)
A machine learning model designed to generate realistic data by learning patterns from existing training datasets. It uses an unsupervised learning framework by using deep learning techniques, where two neural networks work together. One generates data (generator), while the other evaluates whether the data is real or generated (discriminator).
It is superior to deep learning in generating new data, including realistic images or text due to the processing complexity.

GANS
<img width="3888" height="5184" alt="Gans_8285952" src="https://github.com/user-attachments/assets/00ca5721-7cf3-46ae-adc1-ee86313b1edd" />


### Generator

### Discriminator 

### D-dimensional noise vector

### Adversarial dynamic

### Mode collapse 

## Hybrid models

### Variational autoencoder (VAE) 

### Latent space

### Flow-based model

# Standard level and higher level evaluation part

## Efficiency and hardware support

## Training stability 
In artificial image generation, training stability measures whether an optimization algorithm reliably converges to a minimal loss state without numerical divergence or structural mode failure. In simple words, it is the concept that an artificial intelligence learns smoothly and steadily over time without any errors. 
<img width="952" height="781" alt="image" src="https://github.com/user-attachments/assets/a9cb0801-d845-498b-8d1f-c9543ddd414f" />

Brownlee, J. (2019, February 26). How to use Learning Curves to Diagnose Machine Learning Model Performance. MachineLearningMastery.Com. https://www.machinelearningmastery.com/learning-curves-for-diagnosing-machine-learning-model-performance/
‌
## Neural Network
A neural network is a group of interconnected units called neurons that send signals to one another. Neurons can be either biological cells or mathematical models. While individual neurons are simple, many of them together in a network can perform complex tasks. There are two main types of neural networks.

In neuroscience, a biological neural network is a physical structure found in brains and complex nervous systems – a population of nerve cells connected by synapses.
In machine learning, an artificial neural network is a mathematical model used to approximate nonlinear functions. Artificial neural networks are used to solve artificial intelligence problems.

https://lamarr-institute.org/wp-content/uploads/deepLearn_2_EN.png

## Flexibility and scability 

## Consistency management 

### Character consistency 

### Embedding-based approach

### Style adherence

# Standard level and higher level ethics part

## Dataset curation 

## Bias and fairness 

### Bias mitigation

## Transparency 

