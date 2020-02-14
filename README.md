# StaDynA: Addressing the Problem of Dynamic Code Updates in the Security 
Analysis of Android Applications

# UPDATE: From now on the code is temporary available upon request.
Please, check how to contact me on [my personal website](https://zhauniarovich.com).



## Description
StaDynA is a system supporting security app analysis in the presence of dynamic
code update features (dynamic class loading and reflection).

Our tool combines static and dynamic analysis of Android applications in order
to reveal the hidden/updated behavior and extend static analysis results with
this information.

This work has been done at the University of Trento.




## Publication
The results of our research were presented at the 5th ACM Conference on Data 
and Application Security and Privacy (ACM CODASPY 2015). Please use the 
following bibtex reference to cite our paper:

```
@inproceedings{StaDynA_Zhauniarovich2014,
    author = {Zhauniarovich, Yury and Ahmad, Maqsood and Gadyatskaya, Olga and Crispo, Bruno and Massacci, Fabio},
    title = {{StaDynA: Addressing the Problem of Dynamic Code Updates in the Security Analysis of Android Applications}},
    booktitle = {Proceedings of the 5th ACM Conference on Data and Application Security and Privacy},
    series = {CODASPY '15},
    year = {2015},
    pages = {37--48},
    url = {http://doi.acm.org/10.1145/2699026.2699105},
    doi = {10.1145/2699026.2699105},
    publisher = {ACM}
}
``` 


## Usage
Our tool consists of two parts: a server and a client. The server side of
StaDynA is a Python program that interacts with a static analysis tool. 
Currently, StaDynA uses AndroGuard as a static analyzer. The client side is the
code run either on a real device or on an emulator.

The instructions how to build client side can be found in the corresponding 
folder.

To run the analysis of an Android application, after connecting a device running
client side, execute the server side Python script:

```
python stadyna.py -i <inputApk> -o <resultFolder>
```

where *inputApk* is a path to the apk file to be analyzed, and *resultFolder* is
the path where the results of the analysis will be stored.


## Dependencies
1. [networkx](https://networkx.github.io/) released under BSD license.
2. [AndroGuard](https://code.google.com/p/androguard/) released under Apache-2.0
license.


 
## License
The tool is distributed under Apache-2.0 license. The citation of the paper is 
highly appreciated.
