# Introduction to the step-by-step guide

Here are step-by-step instructions on how to run the FlowJo stat workflow.  
This workflow allows the automation and parallelization of many plot analyses.

# Create Project

Create a Project in Tercen  
Note: If you create in a Team, then you can share it easier

# Preparation of the three files

You require three files

* Measurement file  
* Sample annotation file  
* Display name file

These can be created from the Flowjo Export Table file

Here is a link to a template of the three files.  
Download them and fill them out.

# Uploading the data {#uploading-the-data}

When uploading the data:

* ATP import as “character”  
* SEB import as “character”  
* Days import as “character”

# Finding the template

I copied it from a project.

# Open the workflow

## Gather Step

* Remove all and add all

## Join Step

Run the join

## Wizard Step

| Question | Action | Remark |
| ----- | :---: | ----- |
| "Select the samples column from the measurement file (i.e., FlowJo file). Examples: \`samples | samples | Had to select |
|  "Select the samples column from the sample annotation file. Examples: \`sample.samples\`  | sample.samples | Automatically selected |
| "Select the ELN column from the sample annotation file, otherwise, leave blank. Examples: \`sample.ELN\`",  | sample.ELN | Had to select |
| No selection necessary, click Next | exp.variable | Automatically selected |
| No selection necessary, click Next | cellpop.Flowjo name | Automatically selected |
| No selection necessary, click Next | cellpop.Display name | Automatically selected |
| No selection necessary, click Next | Cell.pop Display name  “NA” “ “ | Automatically selected |
| No selection necessary, click Next | cell.pop.Display name “NA” “ “ | Automatically selected |
| No selection necessary, click Next | exp.value | Automatically selected |
| "Select the factors representing the conditions. Multiple selections are possible. Examples:  \`sample.compound\`, \`sample.ATP\`, \`sample.Ab\`, \`sample.Ab2\` and etc..",  | sample.Ab sample.Ab2 sample.treatment sample.STP sample.SEB  | Manually selected |
| Selecting the control per condition (z-score on mean) Filters \- Select your control compound/condition | sample.treatment \= DMSO ATP \=0 SEB \=1 Ab= PD1 Ab2 \= Belrestotug | Manually selected Apply filter |

## Checking if all the annotations are correct

Checking if there is one single value per cell

## Create Filter

# Customization of Plots

| Point plot | 2Gb |
| :---- | :---- |
| Barplot (mean) with jitter | 2Gb |
| Barplot (mean) with sd error bars | 2Gb |
| Heatmap | 2Gb, 1000x3000 |

# Download the Data and Plots

