#Deduplication Problem

Given Task: To identify unique patients in a given hospital record on the basis of given parameters

#Python Libraries used:
* Dedupe (https://github.com/dedupeio/dedupe)
* Pandas
* Numpy
* csv
* os
* other relevant libraries

#Files generated
1. Deduplication Problem-Sample Dataset.csv (input file)
2. max.csv (actual file which we use)
3. csv_example_training.json (training file)
4. output.csv (output file) 
5. Duplication.ipynb

#Dataset description
Dataset contains data of 103 patients ( in which many are duplicates ),with fields = {ln,fn,dob,gn}

###Brief working

#Dataset cleaning
Dataset has no missing values, so we need to just do some rearrangements in order to clean the data

#Training 
Now using Dedupe we will train the data, but it need training data file i.e. csv_example_training.json, to generate this file we will train it through active labelling method.
Once trained, we can use this file again or we can also retrain it (if required).

#Clustering
After that we do clustering of datasets which give us list of tuples, along with confidence score. Then we pick relevant features and merge them with other names so that every name covered at least once and then give output.csv as output file.
