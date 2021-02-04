> ### **Introduction**
- Model entered 'ImageNet Large-Scale Visual Recognition Challenge' (ILSVRC-2010/2012)
- Classified 1.2 million images into 1000 classes 


> ### **Architecture**
- 8 learned layers
- 5 convolutional layers
- 3 fully connected layers
- 1000-way softmax
- 60 million parameters
- 650,000 neurons

    >### **GPUs**
    - Trained in parallel on two RTX 580s
    - GPUs communicate in certain, not all, layers

    >### **ReLu**
    - Non-saturating activation function: 
        - ### $f(x) = (0,max)$ 
    - used over saturating nonlinearity, _s.a_ :
        - ### $f(x) = (1 + e^{-x})^{-1}$
        - ### $f(x) = tanh(x)$
    - due to faster training time  
    - Doesn't require input normalisation


    > ### **Local Response Normalisation**
    - Normalisation method for generalisation
        - ## $b^{i}_{x,y} = a^{i}_{x,y} / (k + \alpha \sum_{j=max(0,i-n/2)}^{min(N-1,i+n/2)} (a^{j}_{x,y})$

    - ## $b^{i}_{x,y}$ 
        the response-normalised activity 
    - ## $i$ 
        the $i^{th}$ kernel
    - ## $a$ 
        the current neuron 
    -  ## ($k$, $n$, $\alpha$, $\beta$)
        a set of hyperparameters
    
    > ### **Overlapping Pooling**
    - Pooling layers in CNNs summarise the outputs of neighbouring groups of neurons in the same kernel map
    - Reducing the number of pixels _(s)_ between pooling units, which summarise the inputs of a _(z*z)_ neighbourhood, causes an overlap
    
> ### **Performance**
- Achieved top-1 (37.5%) and top-5 (17.0%) error rates  
- Response normalization reduces our top-1 and top-5 error rates by 1.4% and 1.2%

