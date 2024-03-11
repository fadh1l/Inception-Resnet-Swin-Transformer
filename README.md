## Swin Transformer with Inception-ResNet Patch Merging

This project investigates the performance improvements possible by integrating an Inception-ResNet-based feature extraction module within the patch merging stage of the Swin Transformer architecture.

**Motivation**

* Swin Transformers employ linear embedding for patch merging. Could a more sophisticated feature extraction technique improve performance?
* Inception-ResNet modules excel at capturing features at multiple scales. This might enrich the representation learned during patch merging.

**Modifications**

* The original linear embedding layer in the Swin Transformer patch merging is replaced with an Inception-ResNet module.


**Performance on Retinal OCT Dataset**

| Epoch | Train Loss | Valid Loss | Accuracy | F1-Score | Precision | Recall | Time |
|-------|------------|------------|----------|----------|-----------|--------|------|
| 0     | 0.0783     | 0.0175     | 0.9959   | 0.9959   | 0.9959    | 0.9959 | 09:04 |
| 1     | 0.0789     | 0.0619     | 0.9783   | 0.9784   | 0.9798    | 0.9783 | 09:07 |
| 2     | 0.0600     | 0.0262     | 0.9948   | 0.9948   | 0.9949    | 0.9948 | 09:05 |

* Our study significantly advances medical picture classification and opens the door for more developments. 
* Interestingly, our improved Swin model outperforms other well-known models like Efficient-Swin, VGG16, ResNet18, and AlexNet.


