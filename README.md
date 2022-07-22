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
@article{CacheTest,
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
* C++ run on Windows (SDK higher than 10.0.150630.0)
* CPLEX 12.80 Acamidic version
* at least 8 GB RAM.


## Building

In Linux, to build the version that multiplies all elements of a vector by a
constant (used to obtain the results in [Figure 1](results/mult-test.png) in the
paper), stepping K elements at a time, execute the following commands.

```
make mult
```

Alternatively, to build the version that sums the elements of a vector (used
to obtain the results [Figure 2](results/sum-test.png) in the paper), stepping K
elements at a time, do the following.

```
make clean
make sum
```

Be sure to make clean before building a different version of the code.

## Results

Figure 1 in the paper shows the results of the multiplication test with different
values of K using `gcc` 7.5 on an Ubuntu Linux box.

![Figure 1](results/mult-test.png)

Figure 2 in the paper shows the results of the sum test with different
values of K using `gcc` 7.5 on an Ubuntu Linux box.

![Figure 1](results/sum-test.png)

## Replicating

To replicate the results in [Figure 1](results/mult-test), do either

```
make mult-test
```
or
```
python test.py mult
```
To replicate the results in [Figure 2](results/sum-test), do either

```
make sum-test
```
or
```
python test.py sum
```

## Ongoing Development

This code is being developed on an on-going basis at the author's
[Github site](https://github.com/tkralphs/JoCTemplate).

## Support

For support in using this software, submit an
[issue](https://github.com/tkralphs/JoCTemplate/issues/new).
