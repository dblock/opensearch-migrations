# Upgrade Testing Framework

This package is built on the `cluster_migration_core` library and provides runnable steps to test ElasticSearch and OpenSearch upgrades

## Running the Upgrade Testing Framework

To run the UTF, perform the following steps

### PRE-REQUISITES

* Python3 and venv
* Currently in the same directory as this README, the setup.py, etc

### Step 1 - Activate your Python virtual environment

To isolate the Python environment for the project from your local machine, create virtual environment like so:
```
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

You can exit the Python virtual environment and remove its resources like so:
```
deactivate
rm -rf .venv
```

Learn more about venv [here](https://docs.python.org/3/library/venv.html).

### Step 2 - Run the UTF
Run the UTF framework with the `run_utf.py` script and a test config file. For the default snapshot/restore upgrade from Elasticsearch 7.10.2 to OpenSearch 1.3.6, it can be invoked with:
```
./run_utf.py --test_config test_configs/snapshot_restore_es_7_10_2_to_os_1_3_6.json
```