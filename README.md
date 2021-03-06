# MakeupEmbeddingGAN-tf-Implement
* A tensorflow Implement for MakeupTransfer & MakeupEmbedding based on [cycleGAN](https://github.com/junyanz/CycleGAN/) and [ZM-Net](https://arxiv.org/pdf/1703.07255.pdf)
## Model Design
* Using AdaIN in parallel Pnet(StylePredictingNet) and Tnet(StyleTransferNet) Architecture  
* Learning How-to-Transfer-a-Given-Style in Tnet & Learning What-is-a-Given-Style in Pnet
##### Model Architecture
<div align="center"><img width="50%" src="https://github.com/baldFemale/MakeupEmbeddingGAN-tf-Implement/raw/master/present/Architecture_1.png"></div>  

##### Generator Architecture
<div align="center"><img width="50%" src="https://github.com/baldFemale/MakeupEmbeddingGAN-tf-Implement/raw/master/present/generator_arch.png"></div>  

##### Discriminator Architecture
* Same 70*70 patch discriminator as cycleGAN  

## Loss Function
Following [beautyGAN's](https://dl.acm.org/citation.cfm?id=3240618) setup which includes:
* adversarial loss
* cycle loss
* makeup loss (histogram match loss on face&lip&eye shadow)
* perceptual loss (calculate on relu4_1 of pretrained VGG16 model)

## Results
##### MakeupTransfer Results  
<div align="center"><img width="80%" src="https://github.com/baldFemale/MakeupEmbeddingGAN-tf-Implement/raw/master/present/table.PNG"></div>  

##### Embedding Learned from Pnet Test  
###### Style Fusion
<div align="center"><img width="80%" src="https://github.com/baldFemale/MakeupEmbeddingGAN-tf-Implement/raw/master/present/style_fusion.png"></div>
  


