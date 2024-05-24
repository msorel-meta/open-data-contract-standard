[![OpenSSF Best Practices](https://www.bestpractices.dev/projects/8149/badge)](https://www.bestpractices.dev/projects/8149)

# Open Data Contract Standard (ODCS)

Welcome! 

Thanks for your interest and for taking the time to come here! ❤️

## Executive summary
This standard describes a structure for a **data contract**. It's current version is v2.2.2. It is available for you as an Apache 2.0 license. Contributions are welcome!

## Discover the open standard
Discover the [Open Data Contract Standard](docs/standard.md). This file contains some explanations and several examples. More [examples](docs/examples/index.md) can be found here.

## What is a Data Contract?

### The basics of a data contract
A data contract defines the agreement between a data producer and consumers. A data contract contains several sections:
* Fundamentals.
* Schema.
* Data quality.
* Service-level agreement (SLA).
* Security & stakeholders.
* Custom properties.

![Data contract schema](docs/img/data-contract-v2.2.1-schema.svg "Data contract schema")

*Figure 1: illustration of a data contract, its principal contributors, sections, and usage.*

### JSON Schema

JSON Schema for ODCS can be found [here](https://github.com/bitol-io/open-data-contract-standard/blob/main/schema/odcs-json-schema.json). You can import this schema into your IDE for 
validation of your YAML files. Links below show how you can import the schema:

- [IntelliJ](https://www.jetbrains.com/help/idea/json.html#ws_json_schema_add_custom)
- [VS Code](https://code.visualstudio.com/docs/languages/json#_json-schemas-and-settings)

## Contributing to the project
Check out the [CONTRIBUTING](./CONTRIBUTING.md) file.

## Articles 
 * 2024-02-06 - [Getting started with ODCS](https://medium.com/abeadata/getting-started-with-odcs-3ba790707879)
 * 2023-12-08 - [Why the Need for Standardizing Data Contracts?](https://medium.com/abeadata/why-the-need-for-standardizing-data-contracts-133bc3491148)
 * 2023-11-30 - [Linux Foundation AI & Data - Bitol Joins LF AI & Data as New Sandbox Project](https://lfaidata.foundation/blog/2023/11/30/bitol-joins-lf-ai-data-as-new-sandbox-project/)
 * 2023-11-30 - [AIDAUG - Bitol Joins LF AI & Data as New Sandbox Project](https://aidausergroup.org/2023/11/30/bitol-joins-lf-ai-data-as-new-sandbox-project/)
 * 2023-10-01 - [Data Contracts: A Bridge Connecting Two Worlds](https://medium.com/@atanas.iliev.ai/data-contracts-a-bridge-connecting-two-worlds-404eff1d970d)
 * 2023-09-10 - [Data Contracts 101](https://medium.com/p/568a9adbf9a9)
 * 2023-08-10 - [Welcome to the Open Data Contract Standard](https://jgp.ai/2023/08/09/welcome-to-the-open-data-contract-standard/)
 * 2023-05-11 - [Data Contracts – Everything You Need to Know](https://www.montecarlodata.com/blog-data-contracts-explained/)
 * 2023-05-07 - [Data Engineering Weekly #130 - Data Contract in the Wild with PayPal’s Data Contract Template](https://www.dataengineeringweekly.com/p/data-engineering-weekly-130)
 * 2023-05-06 - [PayPal เปิด Data Contract เป็น Open Source Template ให้ไปใช้งานกัน](https://discuss.dataengineercafe.io/t/paypal-data-contract-open-source-template/581/1)
 * 2023-05-05 - [Jonathan Neo (j__neo ) on Reddit](https://www.reddit.com/r/dataengineering/comments/137glbo/comment/jixw5hj/?utm_source=reddit&utm_medium=web2x&context=3)
 * 2023-05-01 - [PayPal open sources its data contract template](https://jgp.ai/2023/05/01/paypal-open-sources-its-data-contract-template/)

If you spot an article about the Open Data Contract Standard, make a pull request! 

## Vendors

Vendors who natively support the Open Data Contract Standard.

A non-exhaustive list of organizations offering solutions natively compatible with ODCS, such as data catalogs, and data quality platforms.

* [DQC.ai | DQ PLATFORM](https://www.dqc.ai/dqc-platform) - [Enhancing Data Quality with ODCS: A Standard Ensured by the DQ Platform
](https://www.dqc.ai/post/enhancing-data-quality-with-odcs-a-standard-ensured-by-the-dq-platform)

## More

### History
Formerly known as the data contract template, this standard is used to implement Data Mesh at [PayPal](https://about.pypl.com/). Starting with v2.2.0, it is maintained by a 501c6 non-profit organization called [AIDA User Group (Artificial Intelligence, Data, and Analytics User Group)](https://aidaug.org). On November 30th, 2023, [AIDA User Group](https://aidaug.org) and the [Linux Foundation AI & Data](https://lfaidata.foundation/) joined forces to create [Bitol](https://bitol.io). Bitol englobes ODCS and future standards & tools.

### How does PayPal use Data Contracts?
PayPal uses data contracts in many ways, but this [article](https://medium.com/paypal-tech/the-next-generation-of-data-platforms-is-the-data-mesh-b7df4b825522) from the [PayPal Technology blog](https://medium.com/paypal-tech) gives a good introduction.

### Mkdocs mike versioning
To start with using [mike](https://github.com/jimporter/mike) as a tool for versioning the documentation, the following was run:

```bash
pip install mike
cd open-data-contract-standard                    #ensure you are inside the repo
mike deploy --push --update-aliases v2.2.1 latest #set latest version to v2.2.1
mike set-default --push latest                    #by default, users will go to latest
```

#### Deploying a new version
Given that the Github action [here](https://github.com/bitol-io/open-data-contract-standard/blob/main/.github/workflows/docs-site-deploy.yaml) it set to trigger when a new tag version is
created, all that is required is to:
1. [Create a new release](https://github.com/bitol-io/open-data-contract-standard/releases)
2. Put in new tag version for release (follows pattern v*)
3. Once release is created with new tag version, the Github action gets kicked off and mike will deploy the latest documentation linked to latest version tag

#### Delete version
If a version tag was pushed that was incorrect, it can be deleted via:

```bash
mike deploy --push --update-aliases <previous tag version> latest #set latest version to previous tag version
mike delete <incorrect tag> --push
```
