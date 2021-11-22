# Blood-Transfusion

This dataset is originaly from :
Author: Prof. I-Cheng Yeh
Source: UCI
To cite: Yeh, I-Cheng, Yang, King-Jang, and Ting, Tao-Ming, "Knowledge discovery on RFM model using Bernoulli sequence", Expert Systems with Applications, 2008.

This dataset is from a mobile blood donation vehicle in Taiwan. The Blood Transfusion Service Center drives to different universities and collects blood as part of a blood drive. We want to predict whether or not a donor will give blood the next time the vehicle comes to campus.

This dataset contains RFMTC model which is a variation of RFM (Recency, Frequency and Monetary). This model is commonly used in marketing for identifying best customers. In this case, te blood donors. There are 748 donor data, each one included :

    R (Recency - months since last donation),
    F (Frequency - total number of donation),
    Monetary - total blood donated in c.c.),
    Time - months since first donation), and
    Binary variable representing whether he/she donated blood in March 2007 (1 stand for donating blood; 0 stands for not donating blood).
    
We will use TPOT(Tree-based Pipeline Optimization), which is a Python Automated Machine Learning tool that optimizes machine learning pipelines using genetic programming. TPOT will automatically explore hundreds of possible pipelines to find the best one for our dataset. Note, the outcome of this search will be a scikit-learn pipeline, meaning it will include any pre-processing steps as well as the model.

After that, we will see if there are a data with high variance, if so, we have to log normalize it first, then we create model again based on tpot recomendation. 
