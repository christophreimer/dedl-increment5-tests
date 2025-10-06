# Destination Earth Data Lake - Demonstration of Increment#5

## Notebook Gallery

[Gallery](https://destination-earth.github.io/DestinE-DataLake-Gallery/) is maintained on GitHub.

Key features:
- Gallery styling following/aligned to the [DEDL portal](https://data.destination-earth.eu/)
- Filter by tags
- Full text search
- Link to JupyterHub
- Onboarding of additional cookbooks / notebook examples
- Template repository

## Integration of binder service in Jupyterhub
Utilising *"Fancy profiles"* to provide integration of binder with Jupyterhub

Allows to add hooks to check for vulnerabilities, currently not deployed in staging.

Changes to be considered:
- user data has to be moved and mounted in the JupyterLab as separate dir (user_data)

## GPU support in STACK service JupyterHub

Demonstrated by Ignacio --> embeddings.

GPUs can be selected via the following configuration "Server Options -> Local Environment -> JupyterLab GPU".

## GPU support in STACK service Dask

Showcase dask-cuda provided by RAPIDS

Worker docker image: nvcr.io/nvidia/rapidsai/base:25.06-cuda12.8-py3.12

Demo Notebook: [Dask-GPU-example.ipynb](https://github.com/user/repo/blob/branch/other_file.md)

## Usage of DEDL - API Keys
API Keys have been issued by CF. These keys can be used equivalent to user/password.
The difference is only in the authentication flow.

Demo notebook: [Dask-API-Key-access.ipynb](./Dask-API-Keys-access.ipynb)

## S3 Key manager integration
After authentication the S3 key manager API is called to request S3 creds.
Verification that S3 creds are available via command:
```
printenv | grep AWS

s3cmd --access_key=$AWS_ACCESS_KEY_ID --secret_key=$AWS_SECRET_ACCESS_KEY --host=eodata.cloudferro.com ls s3://EODATA
```
