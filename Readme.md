# Compute Parameter Validation

## Description

This project provides an Ansible-based solution to validate critical system configurations on OpenStack compute nodes. It checks the status of the kdump service and ensures key kernel Non-Maskable Interrupt (NMI) parameters (kernel.nmi_watchdog, kernel.panic_on_io_nmi, kernel.panic_on_unrecovered_nmi, kernel.unknown_nmi_panic) are enabled.
These settings are essential for detecting and handling hardware or kernel failures, ensuring the reliability of virtual machines managed by Nova.

## Getting Started

Follow these steps to set up and run the validation on a compute node.

**Prerequisites**

- Ansible is installed on the host (pip install ansible or package manager).
- Root or sudo privileges on the target system.
- OpenStack CLI tools (optional, for context).
- Access to a compute node running a compatible Linux distribution (e.g., RHEL).

## Installation

1. Clone the repository:

`git clone https://gitlab.cee.redhat.com/rlondhe/compute-parameter-validation.git`
`cd nova-parameter-validation`

2. Ensure Ansible is configured to run locally.

**Usage**

1. Navigate to the playbooks directory:

`cd playbooks`

2. Run the playbook:

`ansible-playbook nova_param_check.yml`

3. Review the output for the kdump service status and kernel parameter values. The playbook will fail if any NMI parameter is set to 0.

## Add Your Files

- Create or upload files via the GitLab interface.
- Add files using the command line:

`cd existing_repo`
`git remote add origin https://gitlab.cee.redhat.com/rlondhe/nova-parameter-validation.git`
`git branch -M main`
`git push -uf origin main`

## Test and Deploy
Test the playbook on a staging compute node.

