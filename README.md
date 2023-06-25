# *NoAC*: an automatic builder for knowledge bases and browsers in non-model organisms


### Related paper:

Tzu-Hsien Yang, Chien-Chi Liao, You-Yi Chen, Chun-Lin Hsieh, Wen-Chieh Tsai, Yan-Yuan Tseng, and Wei-Sheng Wu\*, "NoAC: an automatic builder for knowledge bases and browsers in non-model organisms", (Under Review)

## Start the Environment

We recommend using Docker to set up the necessary environments for NoAC. 

Here is an example: 

1. Install the Docker software. If you have already installed the Docker software, please skip this step. 

If you are using Microsoft Windows systems, please follow the instructions <a href="https://docs.docker.com/desktop/install/windows-install/">here</a>.

If you are using Mac OS systems, please follow the instructions <a href="https://docs.docker.com/desktop/install/mac-install/">here</a>.

2. Start the Docker program by double-clicking the Docker icon.

***
Please do not stop the Docker program during the execution of the web service.
***

3. Open the command line interface of your system and type

```
docker pull nmokbc/nmokbc:latest

```

to get the latest version of NoAC.

4. Set up the local web service environment:

```
docker run -ti -p 8000:8000 nmokbc/nmokbc /bin/bash

cd /Django/NMOKBC/

python manage.py runserver 0.0.0.0:8000

```

5. Visit the local *NoAC* website by entering the following sites onto the browser URL block:


```
localhost:8000/input
```

## Steps to Use *NoAC*

Users can specify the information of the non-model organism of interest in the "Input" tab page. Only two steps are required to build the inferred knowledge base for this non-model organism:

![](img/construct.jpg)

1. Upload the following four genome information for the non-model organism of interest:

>* genomic.fna: Genomic sequence
>* genomic.gff: Genomic annotations
>* protein.faa: Protein sequences
>* rna.fna: transcript sequences
>* data_table.tsv: summary table generated by NCBI

These files can be downloaded from the NCBI website:

(1) Download *genomic.fna* and *genomic.gff*:
![](img/Download.jpg)

(2) Download *protein.faa*, *rna.fna*, and *data_table*:
![](img/Download2.jpg)

2. Select the referenced model organism and press submit.

The data processing steps may take several hours to proceed. After finishing the data processing steps, the web query interface for the non-model organism knowledge base can be accessed via the provided link. 

## Constructed Non-model Organism Query Interfaces

The constructed of a new knowledge and its query interface may take several hours. In the "Result" tab page, users can type in the existing Job IDs to link to the constructed query interfaces. And the existing knowledge base on the user's computer are also listed in this tab page.

![](img/Result.jpg)