# Computer Science Communication

- Student Name: Haozhen Shen
- Student #: 1003115112

## Sharing

Comfortable sharing through any source.

# Image Super Resolution Using SRGAN

## The problem
Super-resolution is the process of improving and refining the details within an image. Usually we take a low-resolution image as input and aim to output the same image but in higher resolution and with more refined details. However, the refined details are often unknown. This ill-posed problem is in general very challenging sice we could have multiple hight resolution images as the solution to one low resolution image. In the context of this blog post we focus on single image super resolution (SISR). 

We state the problem more formally. Given a degradation process, $$D(I, \delta)$$ where $$I$$ is the image and $$\delta$$  our parameters. Our LR image $$I_x$$ is obtained from degrading our HR image $$I_y$$. 

$$I_{x} = D(I_y, \delta)$$

 Where the degradation process $$D$$ is generally unknown. We aim to find the SR model $$F$$,
 
$${\hat{I}}_y=F(I_x, \theta)$$

Where $$\theta$$ is parameter for our SR model $$F$$. As a result, the objective of Image super-resolution becomes,

$$\hat{\theta}=\underset{\theta}{\mathrm{argmin}}{L({\hat{I}}_y,\ I_y)+\lambda\phi(\theta)}$$

where $$L(\hat{I}_y, I_y)$$ represents the loss function between the generated HR image $$\hat{I}_y$$ and the ground truth image$$ I_y$$ , and $$\phi(\theta)$$ is the regularization term and $$\lambda$$ is the tradeoff parameter.

This is a complex image processing task, which requires us to reconstruct the corresponding high-resolution images from the observed low-resolution images. In this blog we will consider a generative approach based on deep learning to tackle this problem.

## SRGAN

![alt text](http://url/to/img.png)
