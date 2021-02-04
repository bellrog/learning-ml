> ## Intro
- Renewed interest in convnets 
- Larger training sets with millions of labels
- Powerful GPU implementation
- Better regularisation 

> ## Contributions 
- Novel visualisation of intermediate feature layers and of the classifier 


> ## Changes to AlexNet
    - Reduced size of first conv layer from 11x11 to 7x7
    - Reduced data exchange between parallel GPUs

   > ## Deconvnet
    - Unpooling: max pooling is irreversible so the local maxima from the previous conv layer 
    are recorded for later approximations of inverted pooling

    > ### Feature Invariance 
        -  
> ## Conclusions:
- Depth of network, breadth of kernels and resolution of images contribute to accuracy