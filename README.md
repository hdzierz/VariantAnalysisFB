# Variant Calling Pipeline

## How to use

**Step1:**
```
git clone https://github.com/PlantandFoodResearch/PFRAutomatedWorkflows
cd PFRAutomatedWorkflows/VariantAnalysis 
```

**Step 2:**

The pipeline is preconfigured with test data. Be aware that the test data uses uncleaned raw data. You can run the QC pipeline first to get clean test data into the pipeline.

```
nextflow run .
```

**Step 3:**

In the next step you need to configure the run using the file nextflow.config


```
reads = "$baseDir/../KiwiTestData/*R{1,2}.fq.gz"
genome = "$baseDir/../KiwiTestData/kiwitest.fasta"
```

**Step 4**

Run the pipeline:

```
nextflow run .
```

**Step 5**

The hope is that the pipeline ran fine and that the results are OK. If not you might have to do some advanced configuring.






