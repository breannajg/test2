# bg_cicd_template_test

**Lead Data Scientist:** Breanna George

A template for automated Databricks CI/CD pipeline creation and deployment using Azure DevOps and Databricks that triggers unit and integration test cases.

## Repo structure

```
.
├── .azuredevops
│   ├── deploy-job.yml
│   ├── integration-test.yml
│   ├── pull_request_template.md
│   └── repo-ids.yml
├── .coveragerc
├── .gitignore
├── deploy.py
├── pytest.ini
├── README.md
├── setup.cfg
├── unit-requirements.txt
├── VERSION
├── conf
│   └── deployment.json
├── docs
│   ├── Project Charter.md
│   └── Project Exit Report.md
├── reference
│   └── Data Dictionary.xlsx
└── bg_cicd_template_test
    ├── conf
    │   └── logging.py
    ├── jobs
    │   └── score.py
    └── notebooks
        ├── data/
        ├── features/
        ├── training/
        └── viz/
```

Some explanations regarding structure:

* `.azuredevops/` contains the YAML files that define the CI/CD pipelines to trigger Databricks activity based on repo activity.
* `conf/deployment.json` contains configuration on how to deploy jobs into Databricks (cluster size, libraries, etc.), including the Integration Test job performed as part of the Pull Request process.
* While all these folders will appear inside Databricks repos, only the subfolders inside `bg_cicd_template_test` will contain notebooks.
    * `bg_cicd_template_test/conf/logging` configures Python logging agents so you don't have to.
    * `bg_cicd_template_test/jobs` contains the notebooks that will be run as Databricks jobs. As a start we include an empty `score` notebook.
    * `bg_cicd_template_test/notebooks` is the main folder for development work, subdivided by common task types.
* `deploy.py` contains the code that will actually perform the Databricks jobs deploy. This is run by the Azure DevOps pipelines.
* `docs/` is where to store any project-related documentation.
* `README.md` contains this portion of the Repos documentation as a helpful reminder.
* `references/` is the place to store data dictionaries, research papers used, supporting materials from the business, etc.
* `setup.cfg` store Python-specific configurations and metadata.
* `unit-requirements.txt` contains the Python packages needed by `azure-pipelines.yml`
* `VERSION` stores the version of the project. This is used to tag commits whenever a new commit is made against the `main` branch.
