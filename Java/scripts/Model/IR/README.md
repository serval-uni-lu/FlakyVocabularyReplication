# Scripts about IR appraoch to get the CUT

## 1. buildDataset.py

`python3 buildDataset.py [path/to/TEST_folder] [path/to/METHOD_folder]`

#### Features

* Open [path/to/TEST_folder] and [path/to/METHOD_folder] containing body of tests and methods, generated by MetricExtractor.
* Build dataset of methods with ClassName, MethodName, Body and Label (test or CUT method)
* Save file to `dic.json`

## 2. testSKlearnProcessing.py

`python3 testSKlearnProcessing.py [path/to/dataset.json]`

#### Features

* Open dataset created before.
* Create a TfidfVectorizer, fit it on whole TESTS + METHODS
* Use this representation for each tests and methods, then compute the similarity
* Return closest methods to a test
