# Overview of GAN Structure 
A generative adversarial network (GAN) has two parts:

 - The generator learns to generate plausible data. The generated instances become negative training examples for the discriminator.
 - The discriminator learns to distinguish the generator's fake data from real data. The discriminator penalizes the generator for producing implausible results.

## Training process of GAN 

 - When training begins, the generator produces obviously fake data, and the discriminator quickly learns to tell that it's fake.
 - As training progresses, the generator gets closer to producing output that can fool the discriminator.
 - Finally, if generator training goes well, the discriminator gets worse at telling the difference between real and fake. It starts to classify fake data as real, and its accuracy decreases.

<img src="https://github.com/BhanuPrakashPebbeti/Anime-Generation-using-GAN/blob/main/images/gan-training-overview.png" width="600" height="400">

## Here's a picture of the whole system:
<img src="https://github.com/BhanuPrakashPebbeti/Anime-Generation-using-GAN/blob/main/images/generative-adversarial-network.png" width="800" height="400">

 - Both the generator and the discriminator are neural networks. The generator output is connected directly to the discriminator input. Through backpropagation, the discriminator's classification provides a signal that the generator uses to update its weights.
