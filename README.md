[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1bVtTmbMLnfFBv44rPwmBFsHvpX7woDWn?usp=sharing)
![Deployment Pipeline](https://github.com/biosimulators/bsvs/actions/workflows/pipeline.yml/badge.svg)
[![Documentation](https://readthedocs.org/projects/bsvs/badge/?version=latest)](https://bio-compose.readthedocs.io/en/latest/)

# **Biological Simulation Verification Service (`bsvs`)**: A high-level Python client for the Biological Simulation Verification Service REST API.

## **Documentation**: 

The complete `bsvs` documentation can be found here: https://bsvs.readthedocs.io/en/latest/

## **Getting Started**:

We recommend using poetry to install this tooling. Installation of this tooling can be performed using PyPI as such:

```bash
pip install bsvs
```

#### Alternatively, **the REST API can be accessed via Swagger UI here: [https://biochecknet.biosimulations.org/docs](https://biochecknet.biosimulations.org/docs)**

### **_IMPORTANT NOTES_**:
- Poetry is used as the environment manager. Poetry uses a globally referenced configuration whose cache setup may lead to permission errors when running `poetry install`. In the event that such errors exist, run the following:
```bash
poetry config cache-dir ~/poetry-cache
mkdir -p ~/poetry-cache
chmod -R u+w ~/poetry-cache

# then install the project:
poetry install
```
- If you are using the jupyter notebooks found within `/tests`, you must link the environment (in this case `poetry`) to the notebook's kernel. Take the following steps to ensure such linking occurs:
```bash
# in the case of running (poetry config virtualenvs.in-project true), the env name will be .venv
poetry run python -m ipykernel install --user --name=$ENV_NAME --display-name "$ENV_NAME"
```

