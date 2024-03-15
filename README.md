# sangeetashukla.github.io
Personal site for content collection


# CFDE Cloud Workspace Partnership (CWP) Pilot
## Overview of CWP Pilot
Our goal with the Kids First CFDE “Cloud Workspace Partnership Pilot” is to understand valuable data, tool and research use cases of other CFDE DCCs and collaboratively pilot integration of data and tool usage in the [CAVATICA cloud workspace](https://www.cavatica.org/).  At its core, the pilot is focused on demonstrating the value of a collaborative and interoperable cloud workspace for the CFDE and broader Common Fund community that supports integrated CFDE dataset analysis in the cloud and supports cross DCC use cases that matter to investigators.

During these piloting activities, we aim to provide dedicated support to DCCs and their users, with the goal of not only successfully [demonstrating solutions](https://docs.cavatica.org/docs/collaborating-on-cavatica-a-guide-for-consortia) for specific cloud data accessibility using [GA4GH DRS](https://docs.cavatica.org/docs/import-from-a-drs-server) and [other methods](https://docs.cavatica.org/docs/upload-your-data-to-cavatica) to enable analysis use cases from multiple DCCs, but also improving [training resources](https://docs.cavatica.org/docs/build-a-workflow-tutorial) and [documentation](https://docs.cavatica.org/) to maximize ease of understanding, accessibility and reusability for the Common Fund community in future efforts.


## Why Choose Cloud-Based Analysis?
High performance computing necessary for genome-scale analysis requires advanced computer infrastructure. By networking a collection of servers and storage devices, researchers can utilize these machines to carry out the large-scale calculations and computations required for genome alignment and variant calling. High performance computing incurs large upfront costs associated with purchasing equipment as well as ongoing costs associated with staff to maintain this environment and electricity to keep everything running.

Cloud-based computing allows access to this same infrastructure without owning and managing the machines themselves. Rather than purchase the computers themselves, users of cloud computing pay to work in this environment on an amount relative to their usage. Dozens of machines can be activated rapidly when an analysis is beginning - and then shut off just as quickly once the work is complete and they are no longer needed.
CAVATICA provides the service of activating and deactivating these computers when called upon by its users. This allows researchers to focus on the biological and bioinformatic aspects of their project, such as experimental design and analysis, without having to set up cloud infrastructure from scratch.

Data analysis requires genomic files to be in the same location as the software tools that are processing them. The increasing scale and size of genomic data is becoming a burden to moving these files onto an institutional location where the software has been installed. Cloud-based analysis offers an alternative – move the relatively small software files to the location where the data is stored.

Furthermore, cloud computing also allows users to share data seamlessly with collaborators. Any collaborator can create an account and receive access to the same platforms. Useful data products, tools, and results can also be quickly disseminated and shared with the broader research community following publication.


## Exploring and Accessing Datasets

---
### Overview of Accessing Data in CAVATICA

There are a variety of data access tiers across different DCCs. These tiers span a range of open access to controlled access, with file management and access mechanisms ranging from DRS, https pointers to data files, to download / copy of actual files (e.g. FTP). We are matching up these existing tiers with different ways that CAVATICA can support a DCC to provision their data into a cloud workspace where a researcher can then begin their analysis.

![image](https://github.com/kids-first/cloud-workspace-partnership-pilot/assets/1084749/27b1f578-8722-48f7-95f5-de743e21aa71)

One of the commonly used methods for cloud data access is the GA4GH Data Repository Service (DRS) API
- DRS is a set of standardized API calls so data consumers can “an access data in a single, standard way regardless of where it’s stored and how it’s managed”.  
- DRS can be utilized for both controlled access an open access data, but has become a core standard as part of NCPI for controlled access. 

### Controlled Access Data for Secondary Use
Users interested in data from DCCs who submit their data to dbGaP for controlled access can use the dbGaP DRS/RAS integration with CAVATICA

[dbGaP - Tips for Preparing a Successful Data Access Request](https://www.ncbi.nlm.nih.gov/projects/gap/cgi-bin/GetPdf.cgi?document_name=GeneralAAInstructions.pdf)

[![dbGaP: Apply for Controlled Access Data](https://img.youtube.com/vi/m0xp_cCO7kA/0.jpg)](https://www.youtube.com/watch?v=m0xp_cCO7kA)

---
### Consortium Controlled Access Data
Leveraging shared private workspaces for DCC hosted data will be the preferred option for prototyping successful analysis during the pilot. Hosting own DRS server will need integration with CAVATICA for authentication/authorization.

---
### Open Access Data
There are a number of options for users to access open data from DCCs
- Open DRS server managed by DCC
- Use CAVATICA DRS services once DCC has indexed their data on CAVATICA DRS server
- Access non-DRS sources such as open access cloud storage (including AWS Open Data)

---
### Bring Your Own Data

You can upload your private data to CAVATICA using any of the following file transfer methods to suit your various requirements and achieve the best upload speed and reliability for the volume and structure of data that you are uploading.

#### Upload from your local storage 

##### Upload directly through CAVATICA's visual interface

The easiest and most intuitive way of uploading files to CAVATICA is to use the integrated upload functionality. This allows you to browse and select files from your local storage and upload them directly, without using additional tools or services. This upload method is most convenient and demonstrates best performance for small-scale uploads.

##### Upload using the Command-line (CLI) Uploader

If you have a larger volume of data on your local machine or cluster and want to upload it to CAVATICA (store it in CAVATICA storage), use the [Command-line (CLI) Uploader](https://docs.cavatica.org/docs/upload-via-the-command-line). The CLI uploader is a fast and secure upload client that has been optimized to efficiently upload files to CAVATICA, taking advantage of parallelization where possible.

If the two recommended methods above are not convenient or suitable for your use case, you can also consider the following alternative upload option to bring data from your local storage to CAVATICA:

##### Upload via the API
If you want to implement your own upload mechanism, you can use the [CAVATICA API](https://docs.cavatica.org/docs/upload-files) as a low-level method of uploading data to CAVATICA that treats a file as an ordered collection of smaller parts, manipulates multipart uploads, and offers more direct control over uploads.

##### Import from cloud storage
If the data you want to bring to CAVATICA is located in a cloud storage service, rather than your local machine, here are the import methods you can use depending on the location of your data.

##### Import from a volume
If the data is already available on a cloud storage service (AWS S3 or Google Cloud Storage) and you want to use it on CAVATICA without transferring it to CAVATICA storage, use the [Connect Cloud Storage](https://docs.sevenbridges.com/docs/connecting-cloud-storage-overview) feature.

##### Upload from an HTTP(S)/FTP server
If the data is available on an FTP or HTTP endpoint and you want to upload it to CAVATICA (store it in CAVATICA storage), use the [HTTP(S)/FTP](https://docs.cavatica.org/docs/upload-from-an-ftp-server) upload option. 



## Applying for Collaborative Project Funding
###

We are happy to announce the launch of the CFDE “Cloud Workspace Partnership Pilot” for the extended CFDE user community to collaboratively pilot integration of data and tool usage in the CAVATICA cloud workspace. Preference will be given to applications with cross-analysis of data sets from multiple CFDE DCCs. The initial award will cover $1000 of cloud costs with additional support subject to further review.

During these piloting activities, you will receive dedicated support to bring your data and analysis to the CAVATICA cloud workspace using a range of methods including GA4GH DRS, in addition to training resources and documentation. Once you create your login, you may want to explore [public projects](https://docs.cavatica.org/docs/bulk-rna-seq-transcription-profiling-of-hsv-1-infected-cells) to review fully documented examples of analyses on CAVATICA.

We recognize the value and importance of the community’s rich variety of research use cases and accompanying data analysis needs.  In order to empower use case piloting in CAVATICA, members from the diverse user community can apply for funding for collaborative pilot projects to offset cloud compute and storage costs. The collaborative projects will also receive support and guidance from the Kids First and CAVATICA Outreach and bioinformatics teams to help meet their goals successfully.

In order to apply, please follow the steps below:

1. First prepare Your Application Submission Content
Information you will be asked to provide when you submit your application includes
- ___Name___ (your first and last name)
- ___Affiliation___ (your organization or academic affiliation)
- ___Email___ (the email address at which we can reach you)
- ___CFDE DCC(s)___ (CFDE Data Coordinating Center names whose datasets you plan to use)
- ___CFDE Datasets___ (specific CFDE datasets you plan to use)
- ___Non-CFDE Datasets___ (specify any non-CFDE datasets, if you plan to use datasets which are not from CFDE Data Coordinating Centers)
- ___Research Description___ (describe your proposed research, limiting to 150-350 words)
- ___Technical Plan___ (describe your proposed technical plan, limiting to 100-200 words)
- ___Budget Amount and Justification___ (describe the planned budget and its justification)

2. Submit an [online application](https://forms.gle/L4mJsUesTRaH1SdQ7).

For more information or feedback about the “Cloud Workspace Partnership Pilot” program, on [CFDE Slack](cfdeworkspace.slack.com) reach out in the #cloud-workspace-pilot channel or send an email to Surya Saha (surya.saha@velsera.com) and Eric Wenger (wengere@chop.edu).

## Estimating Cloud Computing Costs


Any analysis that has been performed locally can be run in the cloud. These could include large-scale workflows, such as genome alignment or gene expression quantification. They also could include smaller operations in an interactive session – reviewing the alignment in a genome browser or building a volcano plot from the gene expression values in the Data Cruncher’s R Studio.

The Seven Bridges CAVATICA environment is built upon [Amazon Web Services (AWS)](https://aws.amazon.com/) and [Google Cloud Platform (GCP)](https://cloud.google.com/). The CAVATICA cloud infrastructure pricing guide describes details of pricing for compute and storage for [AWS](https://aws.amazon.com/) and [GCP](https://cloud.google.com/)

---
### Storage and Compute
Users of cloud computing broadly pay for two categories of usage: ___storage___ and ___compute___.

___Storage___ refers to keeping files stored in the cloud, analogous to storing files on the hard drive on your computer.

All files uploaded to a CAVATICA project by a user incur storage costs. Additionally, any newly generated output files from user workflows also incur storage costs. The cost of storing files in the cloud is based on the size of the files and the length of time they are stored. Prices fluctuate but are generally around 2 cents per gigabyte per month. The most current rate is available in [AWS's documentation](https://aws.amazon.com/s3/pricing/) and [GCP documentation](https://cloud.google.com/storage/#pricing). It is important to consider the files that will be generated by your workflow, estimate their sizes, and add this to your cloud credits budget.

There are no storage costs for Kids First files on CAVATICA that are accessed through the Kids First Portal using the “Analyze in CAVATICA” button in the File Repository. These include the harmonized genome alignments and variants identified through our workflows that serve as starting points for your analysis.

__Important:__ Any files that incur storage costs – files uploaded by the user, intermediate files generated by bioinformatic workflows, output files, resulting graphs generated through analysis in the CAVATICA Data Cruncher – will continue to incur costs at the conclusion of your project. A clean-up plan is necessary for the conclusion of your project when credits are no longer available to support the storage of these on the platform.

___Compute___ refers to using workflows to run computation on files. Within the CAVATICA environment, this could be running a Task of an App in order to process genome files to call variants. It could also refer to using the Interactive Analysis, such as the Data Cruncher to run R scripts and generate graphical output.

Compute in the cloud is billed on the size of the computer being run and the length of time it is being used. Prices vary based on the scale of the job, with current rates available in [AWS's documentation, linked here](https://aws.amazon.com/ec2/pricing/on-demand/) and [GCP on CAVATICA](https://docs.cavatica.org/docs/cloud-infrastructure-pricing#compute-costs-google-cloud-platform).

---
### Estimating Analyses

___EXAMPLE: Using Existing Kids First DRC Workflows on AWS___

As an example of estimating analyses in CAVATICA, consider the scenario where you were looking to harmonize your existing data with Kids First Datasets.  In such a case, you may be interested in running one of the Kids First DRC's bioinformatic pipelines we use for our harmonized data. The provided costs are estimates used by the Kids First DRC for budgeting purposes for creating our harmonized genomic files using the listed workflows.

__Important:__ Each of the Kids First DRC's pipelines have been run thousands of times to produce the harmonized genomic data resource. Costs vary with each run and are influenced by the availability and price of spot instances and changing rates for cloud computing. We have provided the median cost and interquartile range (IQR - range for the middle 50% of runs) for each pipeline. These values reflect historical trends which can be used for estimating and budgeting future analyses; they do not represent guaranteed costs. Costs in the table are for running the given workflow one time using the given input.

| Pipeline | Input | Workflow | Median | IQR |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| [**Kids First DRC Alignment and GATK HaplotypeCaller Workflows**](https://github.com/kids-first/kf-alignment-workflow) | Alignment in BAM format | _Realignment to CRAM with AggMetrics, WgsMetrics, and gVCF creation_ | $22.90 | $14.70 - $30.40 |
| [**Kids First DRC Alignment and GATK HaplotypeCaller Workflows**](https://github.com/kids-first/kf-alignment-workflow) | Alignment in CRAM format | _gVCF creation_ |  $7.68 | $6.96 - $8.70 |
| [**Kids First DRC Joint Genotyping Workflow**](https://github.com/kids-first/kf-alignment-workflow) | Trio of gVCFs from one family | _VCF Creation_ | $3.67 | $2.54 - $4.61 |
| [**Kids First DRC Somatic Variant Workflow**](https://github.com/kids-first/kf-somatic-workflow) |  Paired Tumor & Normal CRAM Alignments | _4 SNV callers, consensus calling, annotation, CNVs, and SVs_  | $42.50 | $3.06 - $71.50 |
| [**Kids First RNA-Seq Workflow**](https://github.com/kids-first/kf-rnaseq-workflow) | Single-end FASTQ Input | _Alignment, Gene Expression Quantification, Gene Fusion ID_ | $2.26 | $1.57 - $3.76 |

___Bringing Your Own Workflows___

Users can also bring their own workflows into the cloud to analyze Kids First data in their own investigations. CAVATICA supports tools developed in the Common Workflow Language (CWL) with upcoming plans to support the Workflow Description Language (WDL) and NextFlow.

Computation costs in the cloud are a direct function of how long the user is running the computer, billed in dollars per hour. The long it takes the computer to run the assigned task depends on two factors. The nature of the task is of course important, with larger requests taking more time – for example, aligning a genome will take longer than simply generating an index file. Additionally, the size of the input will also influence how long the task takes to complete – a 90 GB genome file will process quicker than a 120 GB genome file.

As such, it is difficult to predict an exact cost of a workflow before it has been run. We encourage you to develop a workflow and test your pipeline on a small number of samples to build an estimate before scaling to a complete analysis with a larger sample size.

EXAMPLE: The Kids First DRC has produced a [__Cloud Cost Estimator__](https://docs.google.com/spreadsheets/d/1_z6JxJxxbZj0qQ2-i6In2XntLkNDLiNB/edit?usp=sharing&ouid=114381528003679826426&rtpof=true&sd=true), a spreadsheet calculator that can predict cloud costs for benchmarked workflows. For computational costs, select AWS Instance from the drop down menu, the average length of time the workflow runs for, and the number of times the workflow needs to be run. For storage costs, enter an estimate for the size of each type of output as well as the number of files that will be produced.
