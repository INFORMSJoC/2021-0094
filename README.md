[![INFORMS Journal on Computing Logo](https://INFORMSJoC.github.io/logos/INFORMS_Journal_on_Computing_Header.jpg)](https://pubsonline.informs.org/journal/ijoc)

# Integrated Backup Rolling Stock Allocation and Timetable Rescheduling with Uncertain Time-Variant Passenger Demand Under Disruptive Events

This archive is distributed in association with the [INFORMS Journal on
Computing](https://pubsonline.informs.org/journal/ijoc) under the [MIT License](LICENSE).

The software and data in this repository are a snapshot of the software and data
that were used in the research reported on in the paper "Integrated Backup Rolling Stock Allocation and Timetable Rescheduling with Uncertain Time-Variant Passenger Demand Under Disruptive Events" by J. Yin, L. Yang, D. Andrea, T. Tang and Z. Gao.
The snapshot is based on 
[this SHA](https://github.com/tkralphs/JoCTemplate/commit/f7f30c63adbcb0811e5a133e1def696b74f3ba15) 
in the development repository. 

**Important: This code is being developed on an on-going basis at https://github.com/JerryYINJIATENG/TARP. Please go there if you would like to
get a more recent version or would like support**

## Cite

To cite this software, please cite the [paper](https://doi.org/10.1287/ijoc.2019.0934) using its DOI and the software itself, using the following DOI.

[![DOI](https://zenodo.org/badge/285853815.svg)](https://zenodo.org/badge/latestdoi/285853815)

Below is the BibTex for citing this version of the code.

```
@article{BARP,
  author =        {Jiateng Yin, Lixing Yang, D'Ariano Andrea, Tao Tang, Ziyou Gao},
  publisher =     {INFORMS Journal on Computing},
  title =         {{Integrated Backup Rolling Stock Allocation and Timetable Rescheduling with Uncertain Time-Variant Passenger Demand Under Disruptive Events} Version v1.0},
  year =          {2022},
  doi =           {10.5281/zenodo.3977566},
  url =           {https://github.com/INFORMSJoC/2021.0094},
}  
```

## Description

This repository includes the computational results, source codes and source data (with no conflict of interest) for the experiments presented in the paper. 

## Requirements
For these experiments, the following requirments should be satisfied
* C++ run on Windows 10 (with SDK higher than 10.0.150630.0)
* CPLEX 12.80 Acamidic version
* at least 8 GB RAM.

## Results
The results for each instance, involving the fleet size of rolling stocks, ATT (unit: second), value of objective function, CPU time and optamality gap, are presented in [results](results) by "NO BRS", "Randomly solution", "LSM" and "ILM", as presented in Table 11.

## Replicating

To replicate the results in [results](results), please follow the instructions below.

### Contents of this repository

#### data files

The folder [data](data) contains all the parameters and samples used in our experiments.

* The data contains five groups. Each group has two .csv files. In each group, the first file [Output_Passenger_Board](data/R10-1440-720/Output_Passenger_Board) specifies the dynamic passenger arriving volumes at each station for each stochastic scenario. The second file [Output_Passenger_Alight](data/R10-1440-720/Output_Passenger_Alight) specifics the cumulative volume of alighting passengers at each station for each stochastic scenario. In addition, some other related parameters are also listed in the data set.
* In each file [Output_Passenger_Board](data/R10-1440-720/Output_Passenger_Board), the first row reports some basic parameter settings, involving the investment cost, number of time units, and instance type. The second row reports the index of stations, from station 1 to station 26. The following rows present the detailed passenger arriving data, from the first scenario to the last scenario. In each scenario, the passenger related data are grouped into blocks. In each block, the first column indicates the index of time units, while each element in the other columns represents the passenger arrival rate at one specific station on each time unit. Notice that each block contains the passenger arriving data in one scenario. For example, the data from row 4 to row 723 represent scenario 0.
* In each file [Output_Passenger_Alight](data/R10-1440-720/Output_Passenger_Alight), the basic settings are the same as those in [Output_Passenger_Board](data/R10-1440-720/Output_Passenger_Board). Differently, each element in this file represents the cumulative volume of alighting passengers (i.e., $\alpha_{it}^w$) in our model.


#### code files

The code files involve two main parts.

##### data generation
The codes in [Data_generation](Data_generation)


### Steps to implement the code
* Adjust the path of libraries ilcplex.h and ilocplex.h in the project as the default path in your PC
* Add linkers and CPLEX libraries to the correct position
* Change the path of input data, involving the number of arriving passengers and alighting passengers in folder [data](data)

## Ongoing Development

This code is being developed on an on-going basis at the author's
[Github site](https://github.com/tkralphs/JoCTemplate).

## Support

For support in using this software, submit an
[issue](https://github.com/tkralphs/JoCTemplate/issues/new).
