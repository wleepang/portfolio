# Open source

## Projects I led or contributed to at AWS

- **[Amazon Genomics CLI](https://github.com/aws/amazon-genomics-cli)** - *CLI, 2021-22, contributor and de facto product manager. Archived 2024; users moved to AWS HealthOmics.* A command-line tool that deploys the cloud infrastructure and runs genomics workflows on AWS, so researchers don't have to build the plumbing themselves.
- **[Genomics Workflows on AWS](https://github.com/aws-samples/aws-genomics-workflows)** - *Reference architecture, 2018-22, top contributor. Archived 2023; superseded by Amazon Omics.* Code and documentation for running genomics workflow engines on AWS; used by ~100+ customers as a starting point.
- **[amazon-ebs-autoscale](https://github.com/awslabs/amazon-ebs-autoscale)** - *Tool, 2018+, contributor. Archived 2024.* A daemon that adds EBS volumes to a filesystem as it fills, so jobs working with large files don't run out of disk.
- **[aws-healthomics-tutorials](https://github.com/aws-samples/aws-healthomics-tutorials)** - *Tutorials, 2023-24, contributor. Active.* Example code for storing, processing, and querying genomic data with AWS HealthOmics, including generating workflows from natural-language prompts.
- **[amazon-ecr-helper-for-aws-healthomics](https://github.com/aws-samples/amazon-ecr-helper-for-aws-healthomics)** - *Tool, 2023, contributor. Archived; replaced by HealthOmics' ECR pull-through cache support.* A helper for using public container images in HealthOmics workflows.
- **[genomics-secondary-analysis-using-aws-step-functions-and-aws-batch](https://github.com/awslabs/genomics-secondary-analysis-using-aws-step-functions-and-aws-batch)** - *Reference architecture, 2019-20, contributor. Archived; replaced by AWS HealthOmics guidance.* A framework for building next-generation-sequencing secondary-analysis pipelines on AWS Step Functions and AWS Batch.
- **[amazon-genomics-cli-demos](https://github.com/aws-samples/amazon-genomics-cli-demos)** - *Demo samples, 2021-22, contributor. Archived.* Notebook demos of what you can do with the Amazon Genomics CLI, starting with profiling workflow performance.
- **[reinvent-2018-wps201](https://github.com/wleepang/reinvent-2018-wps201)** - *Workshop repo, 2018, author.* Materials for my first re:Invent builder session: training a genome-clustering model with Amazon SageMaker on a large open scientific dataset.
- **[sagemaker4research-workshop](https://github.com/wleepang/sagemaker4research-workshop)** - *Workshop repo, 2018, author.* A hands-on workshop for researchers: explore datasets, run SageMaker training jobs, and serve predictions from hosted endpoints.

## Upstream contributions

- **[miniwdl #793: fix asyncio.get_event_loop() error](https://github.com/chanzuckerberg/miniwdl/pull/793)** - *PR, opened Jul 2025, merged.* Fixes `WDL.load()` failing in interactive sessions such as IPython on Python 3.11+, where `asyncio.get_event_loop()` now raises an error.
- **[Snakemake #2324: native AWS Batch support](https://github.com/snakemake/snakemake/pull/2324)** - *PR, opened Jun 2023, closed Mar 2026 without merging.* As Amazon Genomics CLI was being retired, I contributed its AWS Batch execution functionality upstream to Snakemake so it would outlive the project. After Snakemake 8 the maintainer asked for the work to move into an executor plugin, and the official [snakemake-executor-plugin-aws-batch](https://github.com/snakemake/snakemake-executor-plugin-aws-batch) now exists, so the PR was closed in its favor.
- **[miniwdl-aws #8: GPU resource requests](https://github.com/miniwdl-ext/miniwdl-aws/pull/8)** - *PR, opened Jun 2022, merged.* Lets WDL tasks request GPUs when run on AWS through miniwdl.
- **[Nextflow #1594: AWS CodeCommit support](https://github.com/nextflow-io/nextflow/pull/1594)** - *PR, opened May 2020, merged.* Lets Nextflow pull pipelines directly from AWS CodeCommit git repositories.

## Personal projects

- **[DesktopDeployR](https://github.com/wleepang/DesktopDeployR)** - *R framework, 2016-22, author. 437 stars.* Packages an R application with a portable R environment and a private package library, so people can run it as a desktop app without installing anything system-level.
- **[shiny-directory-input](https://github.com/wleepang/shiny-directory-input)** - *R package, 2021, author. 49 stars.* A Shiny widget that opens the OS's native folder dialog instead of asking users to type a path; for locally run apps only.
- **[shiny-pager-ui](https://github.com/wleepang/shiny-pager-ui)** - *R/Shiny widget, 2023, author. 28 stars.* A pager input with previous/next and page-number buttons, for paging through data that is too heavy to show in one table.
