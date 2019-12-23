# Rule-Set-2-Azimuth-multiprocessing

Jupyter Notebook containing Rule Set 2 (renamed Microsoft Azimuth) on-target sgRNA scoring (Doench et al., *Nat Biotechnol* 2016) with Pandas library and multiprocessing support. 

## Usage

Convert the 'sgRNAs' column to a Numpy array:

`sgRNA30 = random_30['sgRNAs'].to_numpy()`

Run parallelized Azimuth scoring:

`Azimuth = parallelize_dataframe(sgRNA30, parallelize_Azimuth)`

Add scores back to DataFame:

`random_30['Azimuth'] = Azimuth['Azimuth_parallel'].tolist()`

## Dependencies

* Python 2.7
* Pandas
* Numpy
* multiprocessing
* scikit-learn 0.17.1
* Microsoft Azimuth, `pip install azimuth`

## Source

**Microsoft Azimuth:** https://github.com/MicrosoftResearch/Azimuth
