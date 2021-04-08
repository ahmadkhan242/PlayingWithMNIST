# Playing With Mnist
***
## Overview 

### Task 1
* Dataset -   
  Dataset contains 62 folders with 40 images in each folder [Link to dataset](https://www.dropbox.com/s/pan6mutc5xj5kj0/trainPart1.zip)
  * Pre-Processing used -  
      Images were resized to 32x32 to reduce computational power.  
      Images were converted to grayscale(single channel) so that we have data consistency for other tasks.
  
* CNN Architecture - 
  ResNet with four layers two CNN were used followed by three linear layers.
  
  <details> 
    <summary>Complete Architecture summary</summary>
    
  ```bash
        ----------------------------------------------------------------
                Layer (type)               Output Shape         Param #
        ================================================================
                    Conv2d-1           [-1, 64, 32, 32]             576
               BatchNorm2d-2           [-1, 64, 32, 32]             128
                    Conv2d-3           [-1, 64, 32, 32]          36,864
               BatchNorm2d-4           [-1, 64, 32, 32]             128
                    Conv2d-5           [-1, 64, 32, 32]          36,864
               BatchNorm2d-6           [-1, 64, 32, 32]             128
                BasicBlock-7           [-1, 64, 32, 32]               0
                    Conv2d-8          [-1, 128, 32, 32]          73,728
               BatchNorm2d-9          [-1, 128, 32, 32]             256
                   Conv2d-10          [-1, 128, 32, 32]         147,456
              BatchNorm2d-11          [-1, 128, 32, 32]             256
                   Conv2d-12          [-1, 128, 32, 32]           8,192
              BatchNorm2d-13          [-1, 128, 32, 32]             256
               BasicBlock-14          [-1, 128, 32, 32]               0
                   Conv2d-15          [-1, 256, 32, 32]         294,912
              BatchNorm2d-16          [-1, 256, 32, 32]             512
                   Conv2d-17          [-1, 256, 32, 32]         589,824
              BatchNorm2d-18          [-1, 256, 32, 32]             512
                   Conv2d-19          [-1, 256, 32, 32]          32,768
              BatchNorm2d-20          [-1, 256, 32, 32]             512
               BasicBlock-21          [-1, 256, 32, 32]               0
                   Conv2d-22            [-1, 512, 6, 6]       1,179,648
              BatchNorm2d-23            [-1, 512, 6, 6]           1,024
                   Conv2d-24            [-1, 512, 6, 6]       2,359,296
              BatchNorm2d-25            [-1, 512, 6, 6]           1,024
                   Conv2d-26            [-1, 512, 6, 6]         131,072
              BatchNorm2d-27            [-1, 512, 6, 6]           1,024
               BasicBlock-28            [-1, 512, 6, 6]               0
                   Conv2d-29            [-1, 512, 6, 6]       2,359,296
              BatchNorm2d-30            [-1, 512, 6, 6]           1,024
                   Conv2d-31            [-1, 512, 6, 6]       2,359,296
              BatchNorm2d-32            [-1, 512, 6, 6]           1,024
               BasicBlock-33            [-1, 512, 6, 6]               0
                   Linear-34                  [-1, 256]         131,328
                  Dropout-35                  [-1, 256]               0
                   Linear-36                  [-1, 128]          32,896
                  Dropout-37                  [-1, 128]               0
                   Linear-38                   [-1, 62]           7,998
        ================================================================
        Total params: 9,789,822
        Trainable params: 9,789,822
        Non-trainable params: 0
        ----------------------------------------------------------------
        Input size (MB): 0.00
        Forward/backward pass size (MB): 26.19
        Params size (MB): 37.35
        Estimated Total Size (MB): 63.54
        ----------------------------------------------------------------

  ```
</details>

* Training Methodology -  
  Epoch = 50   
  Learning rate = 0.001  
  Weight decay = 0.0001  
  Training batch size = 32  
  Validation batch size = 64  
  Batch Normalisation and Dropout of 0.7 were used for the task.    
* Results -  
  Max Training accuracy -  
  Max Validation accuracy -  
  Training accuracy on last epoch -    
  Validation accuracy on last epoch -  
    <details> 
    <summary>Loss Graph</summary>
    
  ```bash
      Loss Graph
  ```
</details>
  
