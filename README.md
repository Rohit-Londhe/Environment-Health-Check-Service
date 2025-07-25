# Cluster health check - A pre-update facility

# Description

This project provides a pre-update health check facility for OpenShift clusters, ensuring that clusters are in a stable state before performing updates. It includes scripts and tools to assess cluster health, identify potential issues, and generate reports. This is particularly useful for administrators managing OpenShift environments to avoid update failures.

# Getting Started

To get started with this project, follow these steps:

## Prerequisites

- OpenShift CLI (oc) installed
- Access to an OpenShift cluster with admin privileges
- Python 3.8+ and required libraries (e.g., openshift client)


## Installation

Clone the repository:

`git clone https://gitlab.cee.redhat.com/rlondhe/cluster-health-check-a-pre-update-facility.git cd cluster-health-check-a-pre-update-facility`

Install dependencies:

`pip install -r requirements.txt`

Configure your OpenShift cluster access by setting the KUBECONFIG environment variable or using oc login.


## Usage

Run the health check script to assess your cluster:

`python health_check.py`


This will generate a report detailing cluster status, node health, and potential issues. Refer to docs/examples for sample outputs and detailed usage.

## Add Your Files
- Create or upload files using the GitLab interface.
- Add files using the command line or push an existing Git repository:

`cd existing_repo git remote add origin https://gitlab.cee.redhat.com/rlondhe/cluster-health-check-a-pre-update-facility.git git branch -M main git push -uf origin main`


## Integrate with Your Tools

- Set up project integrations to connect with CI/CD tools or monitoring systems.

## Collaborate with Your Team

- Invite team members and collaborators via the "Manage" > "Members" section.
- Create merge requests for code reviews.
- Enable merge request approvals and auto-merge as needed.


## Contributing
Contributions are welcome! Please:

- Fork the repository.
- Create a feature branch (git checkout -b feature-name).
- Commit changes (git commit -m "description").
- Push to the branch (git push origin feature-name).
- Open a merge request.

Run tests with:
`pytest tests/`

## Authors and Acknowledgment
Rohit Londhe (initial author)
