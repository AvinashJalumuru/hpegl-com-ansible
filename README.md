# Ansible integration - HPE Greenlake Compute Ops Manager 

This repository contains code to interact with HPE Greenlake Compute Ops manager to perform OS deployment, firmware upgrade and BIOS configuration

### Pre-requisites

- ansible 2.12 and above

### Inputs

Input Parameters used by the ansible playbook.

- `hpegl_client_id`: (string) The client ID used for authentication with HPE GreenLake.
- `hpegl_client_secret`: (string) The client secret associated with the client ID for secure authentication.
- `hpegl_group`: (string) The name of the HPE GreenLake group to operate within.
- `hpegl_region`: (string) The region identifier for HPE GreenLake resources (e.g., 'us-west').
- `server_serial_list`: (list of strings) List of server serial numbers to be managed or provisioned.
- `iso_local_image_path`: (string) Local filesystem path where ISO images are stored.
- `hpegl_com_os_job_template`: (string) Identifier for the OS job template to be used in provisioning.
- `hpegl_auth_token`: (string) Authentication token for accessing HPE GreenLake APIs.
- `hpegl_settings_id`: (string) Identifier for the HPE GreenLake settings to be applied.

These parameters are required for configuring and running the Ansible playbook to interact with HPE GreenLake resources.

### Recommendations
1. Use Compute Ops Groups for each openshift cluster in a region
2. Create separate OS settings configuration for each cluster
