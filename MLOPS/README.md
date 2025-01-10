# Introduction 
Data Science Platform Repository. Contains all MLOps pipelines as well as serve as a source control for related code.

# Getting Started
## Environment Selection
Environment selection is done through branches, allowing for different versions of the same models and code to coexist and be used in different environments.
release: prd environment branch
main: pprd environment branch
all other branches correspond to dev, to facilitate collaborative development

## Key Pipeline Variables

### Register Data Asset
dataset_name: display name for new data asset/name if the data asset to update
dataset_type: uri_file or uri_folder
dataset_path: relative or absolute path to file. URL within Data Storage, URI in ML Workspace or path in repository

### Train Model
dataset_name: display name for new data asset/name if the data asset to update
dataset_type: uri_file or uri_folder
dataset_path: relative or absolute path to file. URL within Data Storage, URI in ML Workspace or path in repository
environment_path: path of the environment conda file
display-name: name for the ml run
experiment-name: name for the experiment
folder_name: name of folder within data-science/src where the python scripts are. Can be a path (parentfolder/childfolder)
model_name: name for the registered model 

### Train Custom Model
display-name: name for the ml run
experiment-name: name for the experiment
model_name: name for the registered model 
pipeline_path: path within the repository to the yml file

### Promote Model
model_name: name of model to promote
version: version of model to promote (latest or a specific number)

### Deploy Batch Endpoint
batch_path: relative or absolute path to file. URL within Data Storage, URI in ML Workspace or path in repository
batch_type:  uri_file or uri_folder
endpoint_name: name of endpoint
model_name: name of model to create and endpoint to
version: version of model to create and endpoint to (latest or a specific number)

### Send Batch
batch_path: relative or absolute path to file. URL within Data Storage, URI in ML Workspace or path in repository
batch_type:  uri_file or uri_folder
endpoint_name: name of endpoint

### Set Schedule
run_id: run id of the run that should be scheduled
template_name: name of the chosen schedule template (without the .yml)
# Contribute
Ideally, this should serve as a central repository for all ML and Data Science development.