# Definitions

Here you find almost all the concepts that you need. For context definitions you will require to check the [other markdown document](https://github.com/d-prieto/2027IBComputerScienceCaseStudy/blob/main/Context%20definitions.md).

# Standard level and higher level technical part

## Text-to-image generation

Text-to-image generation is an AI process that turns typed words into custom pictures. It uses machine learning models to understand the meaning of the text prompt and generate an image based on the user’s description, including elements such as objects, people, environments, colours, and artistic styles.

## Conditional image generation

Conditional image generators are models designed to synthesize images under explicit control provided by conditioning inputs, such as class labels, sketches and segmentation maps.

The process of this is by providing an input signal to the AI model and it converts it into a mathematical guide and uses it to shape random visual noise into a matching picture.

(https://www.emergentmind.com/topics/conditional-image-generators)

## Segmentation map 

![](https://www.researchgate.net/profile/Sagi-Eppel/publication/339698501/figure/fig1/AS:865545939320832@1583373641463/Exclusive-instance-segmentation-map-from-the-Vector-LabPics-dataset-The-segmentation-is.png)
source: https://chemrxiv.org/doi/full/10.26434/chemrxiv.11930004.v3


Definition: A segmentation map is a pixel-level output array in computer vision where every pixel in an image is assigned a specific class label or category, effectively partitioning the image into distinct semantic regions.

Types of Segmentation Maps:
Semantic Segmentation Maps: Assign a categorical label to every pixel without differentiating between separate objects of the same class. (Example, all pixels belonging to any pedestrian are labeled simply as "pedestrian.")

Instance Segmentation Maps: Go a step further by not only classifying pixels by category but also separating distinct objects of the same class. For example, multiple people in a crowd receive unique instance IDs (Example, "person 1," "person 2").

Panoptic Segmentation Maps: Combine both approaches, providing a comprehensive pixel-level breakdown where countable objects (like cars or people) are separated as individual instances and amorphous (lacking clear form/structure) background elements (like sky, road, or water) are grouped semantically.


## Class labels

Discrete categorical tags that guide generative models to create images belonging to a specific category. So, instead of generating random images, the model can receive an integer or one-hot encoded class label (like "dog", "cat") alongside random noise. The label provides the required category features for the generated output to match. 

## Image-to-image translation
It is a sub-field of computer vision and deep learning where the goal is to map an input image from one domain and an output image in another domain. In simpler words it maps a pattern to another, such as a a winter landscape to a summer landscape.


<img width="1400" height="673" alt="0_Udvw6tGu40iDEkuH" src="https://github.com/user-attachments/assets/30e3141f-8862-40d9-8d91-9e215255c218" />
<img width="431" height="464" alt="images" src="https://github.com/user-attachments/assets/b55938e7-4903-4624-a92b-9c72effadff4" />
Note: the Van Goh joke isn't image-to-image translation because it isn't replacing nor translating visual elements, the images are fundamentally distinct even if they are similar.




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
It works by passing data through different layers. In image processing, small filters called kernels move across the image to detect features such as edges, colours and shapes. These features are passed through deeper layers, which can recognise more complex patterns and objects. Finally, the network uses the information it has learned to make a prediction. During training, it adjusts its weights and kernels to reduce errors and improve accuracy. It is useful for images because CNNs can automatically detect important visual features such as edges, shapes, textures and objects. They also keep the spatial relationship between pixels, which helps the network understand where features are located in an image.
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
The generator's sole purpose is to map random noise to a specific data distribution. In other words it is a master forger, it summons realistic images out of thin air. However, the random noise isn't simply noise, it's called latent space: an N-dimensional space. Moreover, it selects a random point in that space and map it to a specific image. Each dimension changes a very specific value, for example dimension 42 could change solely the lighting intensity. An analogy would be it makes a stew (the image) by combining all the chosen ingredients (the values for each dimension).

The process the generator uses to create images

The process the generator uses to create images
Step1:
<img width="720" height="720" alt="720X720-soup-alla-shroomie-col-1" src="https://github.com/user-attachments/assets/fe41ed69-7e0c-417c-bf1e-b9ee69e0562a" />
Step 2:
<img width="800" height="400" alt="mystical-d-background-powerful-summoning-circle-glowing-ethereal-energy-hooded-figures-chant-ancient-spells-as-swirling-369195367" src="https://github.com/user-attachments/assets/9887a1f3-5f9f-403c-888b-b61dc1f6482f" />


### Discriminator 
A strict art critic whose sole job is to tell the difference between real data and the generator's fake creations. It examines samples from both sides and assigns a probability score of being real or fake. As it improves, it forces the generator to improve; which makes the discriminator increase: hence a positive loop.
### D-dimensional noise vector
This is a raw input array containing random numbers across N-different axes, serving as the raw creative seed for the generator. Like a recipe with N ingredients, each value in the vector specifies a very specific feature. Tweaking even one of these numbers subtly shifts traits like texture, scale, or color across the generated sample.
### Adversarial dynamic
Competitive tug-of-war between the generator and the discriminator, where each network pushes the other to improve. The generator tries to fool the critic with increasingly convincing fakes, and the critic becomes better as discerning fakes. Both networks co-evolve until the generated outputs become nearly indistinguishable from reality.
### Mode collapse 
When the generator gets lazy and finds a single output that consistently fools the discriminator, causing it to completely ignore the rest of the data distribution. Instead of producing a wide variety of realistic samples, it repeats the exact same output or a very narrow range of variations. The model forgets how to create diversity, trapping itself in a very narrow view.
## Hybrid models

### Variational autoencoder (VAE) 

Type of artificial neural network that learns to encode data into/decode from a simpler form. Combines probabilistic latent space representations with deterministic architectures. Unlike traditional autoencoder, represent data as a probability distribution rather than a single point. That allows for it to learn the underlying patterns of data and generate new examples. 

The encoder utilizes input data to map it to a probability distribution in a latent space, which is a simpler representation of the data.
Decoder takes a sample from this latent space and reconstructs the original data or generated a new example that is similar to training data.

![](https://assets.ibm.com/is/image/ibm/variational-autoencoder-neural-network?fmt=png-alpha)

### Latent space

A multi dimensional space where different labels are places to show correspondence between them, for example, two images of different cats would be closer together than an image of a cat and one of a dog. This is useful because it allows models to compress complex raw data into simplified numerical maps and join similar concepts together into clusters, similarly to OLAP cubes.

![](https://miro.medium.com/v2/0*3BFRAEBNQRHuJfSK.png)

### Flow-based model

Flow based model are models that are provided with two images and output the combination of both.

<img width="1172" height="390" alt="image" src="https://github.com/user-attachments/assets/a43d8adb-e69a-4c97-b1e1-7c19aedc2edb" />

Another way this can also work is with one of the images being a pre-trained concept that the model has learnt through training and is applied to the image.

<img width="1328" height="592" alt="image" src="https://github.com/user-attachments/assets/4a532f72-eed9-4edd-af31-6ee4453b32b4" />

However, in both cases, the quantity of the concept or image can be changed.


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

## Flexibility and scalability 

It refers to how a system handles bigger workloads and adapt to new requirements, as they are key principles for growing systems. Scalability links to vertical (more raw computing power e.g. more machines), and horizontal scaling (Upgrading the computers e.g. better processors or more efficient software).

<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/c8f0d91a-9d72-4bf4-a633-c17c6d67c546" />


## Consistency management 

The process of keeping information, ideas, or elements consistent throughout a project. It helps make sure that different parts of the work fit together and do not contradict each other.

### Character consistency 

### Embedding-based approach

### Style adherence

# Standard level and higher level ethics part

## Dataset curation 

## Bias and fairness 

### Bias mitigation

## Transparency 

Transparency in AI is the ability of models to give reasoning behind choices be open about how they make decisions (this is the goal of interpretable AI models). This opposes the black box theory (where models just allow for an imput and an output, without the working or reasoning that led to the output) and has a big role in the ethics of AI.

<img width="850" height="464" alt="image" src="https://github.com/user-attachments/assets/7802d6fe-4e09-49bf-a3bb-f8602d19e4ca" />
