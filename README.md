# Variant Calling Pipeline

## How to use

**Step1:** Run test

The pipeline is preconfigured with test data. INorder to tst whether the pipeline runs through call vc_pipe without command line parameters:

```

nextflow hdzierz/VariantAnalysisFB

```

If teh piepline does not run through, look into teh log file:

```
.nextflow.log
```

and contact the app steward (helge.dzierzon@plantandfood.co.nz).


**Step 2:** Configure file and sample IDs

```
label,file,lane,read,sample,experiment,date,comments
HW1,kiwitest.1.R1.fq.gz,1,R1,HW1,kiwitest,2016-01-01,This is crap
HW1,kiwitest.1.R2.fq.gz,1,R2,HW1,kiwitest,2016-01-01,This is crap
HW2,kiwitest.2.R1.fq.gz,1,R1,HW2,kiwitest,2016-01-01,This is crap
HW2,kiwitest.2.R2.fq.gz,1,R2,HW2,kiwitest,2016-01-01,This is crap
```

**Step 3:** Run the pipeline

Options:

```
output_dir: publish directory for results ["./"]
inpu_dir: Directory that contains the raw reads ["$baseDir/KiwiTestData"]
genome: Reference genome file (*.fasta) ["$baseDir/KiwiTestData/kiwitest.fasta"]
config: Location of config file ["$baseDir/design.config"]

$baseDir = $HOME/.nextflow/assets/hdzierz/VariantAnalysisFB
```

Typical run with data sitting in $HOME/KiwiTestData

```
nextflow run hdzierz/VariantAnalysisFB --input_dir '../KiwiTestData/' --genome '../KiwiTestData/kiwitest.fasta'
```






