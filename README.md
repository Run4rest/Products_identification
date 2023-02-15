**Project**

Products identification from text descriptions and forecasting of multiple related time series by RNN + FCNN

**Author**: Stanislav Novikov, stanislav.novikov@gmail.com

**Created**: 15.02.2023

**Abstract**

In some cases of retail and supply management there is no exact identifier of product in
shipments. Instead of unambiguous id there are short descriptions with arbitrari
abbreviations and typos. However product identification is required to optimize everyday
operations. One of these cases is described in [1]. In this research I simulate the problem
and develop the idea of the authors to propose:
- solution for extracting maximum information from text descriptions for further forecasting
- NN for forecasting that brings together benefits of FCNN and RNN architectures and might
be more efficient than NN presented by [1]
 
**Pilot project v1.3.pdf** contains a detailed description of this work.

**References**
1. Michael Lingzhi L, Elliott Wolf, Daniel Wintz (2020): Duration-of-stay storage assignment
under uncertainty. Published as a conference paper at ICLR 2020. http://arXiv:1903.05063v3
[cs.LG] 1Feb 2020

**Scripts of this work**

*data simulation eng v1.1.ipynb* This script generates data, simulating the history of shipments to a warehouse.

*model p1 v1.1.ipynb* This script performs product identification. It builds/trains MHA + FCNN model and performs clustering of MHA output. See
Fig.4 of Pilot project v1.2.pdf

*model p2 v1.3.ipynb* This one generates training and test data sets for the FCNN + RNN predictive model,creates and trains the model. Writes the
learning history to the file 'history_p2.txt'

*model p3 v1.3.ipynb* This script generates training and test data sets for the predictive FCNN model, createsand trains a predictive model. The learning
history is written to the file 'history_p3.txt'
