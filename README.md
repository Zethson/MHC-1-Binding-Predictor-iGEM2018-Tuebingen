[![Build Status](https://travis-ci.org/Zethson/MHC-1-Binding-Predictor-iGEM2018-Tuebingen.svg?branch=master)](https://travis-ci.org/Zethson/MHC-1-Binding-Predictor-iGEM2018-Tuebingen)
[![codecov](https://codecov.io/gh/Zethson/MHC-1-Binding-Predictor-iGEM2018-Tuebingen/branch/master/graph/badge.svg)](https://codecov.io/gh/Zethson/MHC-1-Binding-Predictor-iGEM2018-Tuebingen)
[![BCH compliance](https://bettercodehub.com/edge/badge/Zethson/MHC-1-Binding-Predictor-iGEM2018-Tuebingen?branch=development)](https://bettercodehub.com/)

# MHCBoost
Gradient boosted trees based predictor for MHC Class I epitope binding prediction.

How to install
=====
1. <code>git clone https://github.com/Zethson/MHC-1-Binding-Predictor-iGEM2018-Tuebingen</code>
2. <code>python setup.py install</code>
3. <code>mhc-1</code>

Usage
=====
## The CLI - Command Line Interface
```bash
> mhc-1
-p, --dataset_to_predict_path             <arg> file to perform prediction on OR peptide sequence
-o, --predicted_dataset_path              <arg> filepath to save the predicted output file to
-a, --allele                              <arg> allele to perform prediction on
-l, --peptide_length                      <arg> epitope peptide length - usually 9
optional -t, --training_dataset_path      <arg> file for classifier training
optional -s, --silent                     suppresses learning output

```

Examples
=====
Simply provide the answers to the questions asked by our tool.
```bash
> mhc-1 
```
Alternatively, provide input parameters when starting the tool.
```bash
> mhc-1 -p/examples/example_input.txt -o /home/mypc/Desktop/output.txt -a A*02:01 -l 9
```
Supported Alleles
=====
MHCBoost supports 65 alleles. 
HLA-A01:01    
HLA-A02:01    
HLA-A02:02    
HLA-A02:03    
HLA-A02:06    
HLA-A02:11    
HLA-A02:12    
HLA-A02:16    
HLA-A02:19    
HLA-A02:50    
HLA-A03:01    
HLA-A11:01    
HLA-A23:01    
HLA-A24:02    
HLA-A24:03    
HLA-A25:01    
HLA-A26:01    
HLA-A26:02    
HLA-A26:03    
HLA-A29:02    
HLA-A30:01    
HLA-A30:02    
HLA-A31:01    
HLA-A32:01    
HLA-A32:07    
HLA-A32:15    
HLA-A33:01    
HLA-A66:01    
HLA-A68:01    
HLA-A68:02    
HLA-A68:23    
HLA-A69:01    
HLA-A80:01    
HLA-B07:02    
HLA-B08:01    
HLA-B08:02    
HLA-B08:03    
HLA-B14:02    
HLA-B15:01    
HLA-B15:02    
HLA-B15:03    
HLA-B15:09    
HLA-B15:17    
HLA-B18:01    
HLA-B27:05    
HLA-B35:01    
HLA-B38:01    
HLA-B39:01    
HLA-B40:01    
HLA-B40:02    
HLA-B44:02    
HLA-B44:03    
HLA-B45:01    
HLA-B46:01    
HLA-B48:01    
HLA-B51:01    
HLA-B53:01    
HLA-B57:01    
HLA-B58:01    
HLA-B73:01    
HLA-B83:01    
HLA-C05:01    
HLA-C06:02    
HLA-C14:02    
HLA-C15:02    

Performance
=====
MHCBoost has an 5-fold crossvalidated average AUC of 0.899 on the IEDB dataset.
The performance on each allele was compared to the state of the art NetMHCPan. Please refer to [].

License
=====
MIT

Authors
=====
Team iGEM 2018 Tübingen    
Lukas Heumos    
Steffen Lemke    
Alexander Röhl

