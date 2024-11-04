# AWS DMS Management Scripts

This repository contains Python scripts for managing AWS Database Migration Service (DMS) tasks and replication instances. Each script utilizes the `boto3` library to interact with the AWS DMS service, allowing for the creation and deletion of DMS tasks and replication instances.

## Scripts Overview

### 1. `create_dms_task.py`
This script creates a new DMS replication task based on configurations specified in an INI file. It sets up task parameters such as:
- **Table Mappings:** Defines which tables to include and any transformations to apply.
- **Task Settings:** Configures logging, error handling, validation settings, and other task parameters.
  
**Key Functions:**
- Reads configuration details from an INI file.
- Defines table mappings and task settings.
- Creates a DMS task using the provided parameters.

### 2. `delete_dms_task.py`
This script deletes an existing DMS replication task specified by its ARN in the configuration file. 

**Key Functions:**
- Reads task ARN from the INI file.
- Deletes the specified DMS task and prints the response.

### 3. `create_repl_instance.py`
This script creates a new DMS replication instance with configurations specified in the INI file. Key configurations include:
- **Replication Instance Identifier:** A unique name for the instance.
- **Allocated Storage:** The size of storage allocated for the instance.
- **Instance Class and Engine Version:** Specifies the type of instance and the DMS engine version to use.

**Key Functions:**
- Reads configuration details for the replication instance.
- Creates a DMS replication instance using the specified parameters.

### 4. `delete_repl_instance.py`
This script deletes an existing DMS replication instance specified by its ARN in the configuration file. 

**Key Functions:**
- Reads task ARN from the INI file.
- Deletes the specified DMS intance and prints the response.

## Requirements
- Python 3.x
- Boto3 library (`pip install boto3`)
- AWS credentials with permissions to manage DMS resources

## Usage
Ensure that your AWS credentials are set up properly and the configuration INI file contains the required sections and parameters for each script. Run each script from the command line as follows:

```bash
python create_dms_task.py
python delete_dms_task.py
python create_repl_instance.py
python delete_repl_instance.py
```
