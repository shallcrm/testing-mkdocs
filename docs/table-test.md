# Table Test

This is being used to test tables



## Simple Table

| #      | Category                                       | Requirement                                                                                                                                                        | Solution Approach                                                                                                                   |
| ------ | ---------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| MGSO.1 | Management Group and Subscription Organization | Subscriptions (or cloud accounts) will be organized to enable a  hub and spoke network topology in the public cloud landing zone..                                 | Hint – Use hub and spoke network topology in architecture                                                                           |
| MGSO.2 | Management Group and Subscription Organization | The hub subscirption includes Cloud\* Services such as network, logging, identity, etc and the spoke cloud services are where the Client applications will reside. | Hint – Network placement of “shared cloud services” that will be used to manage various client workloads                            |
| MGSO.3 | Management Group and Subscription Organization | Cloud\* Services will be assigned tags to optimize Cloud\* Services consumption and costs.                                                                         | Implication – The hyperscaler’s cloud cost management must appear in the solution                                                   |
| MGSO.4 | Management Group and Subscription Organization | The Cloud\* Services selected by the Client will not have any public IP addresses enabled.                                                                         | Implication – Network                                                                                                               |
| MGSO.5 | Management Group and Subscription Organization | Cloud\* Services will be configured to protect the Client data at rest and data in transit.                                                                        | Implication – “Key Vault” must appear in the solution. Each cloud service used should be tested to ensure client data is protected. |
| MGSO.6 | Management Group and Subscription Organization | Cloud\* Services will be configured to collect audit and logging information.                                                                                      | Implication – Needs to be a logging solution to track changes to the cloud platform at a minimum.                                   |
| MGSO.7 | Management Group and Subscription Organization | the Client DNS will be integrated with Cloud\* Services.                                                                                                           | Implication – Network                                                                                                               |

## Table with Nested Lists

| AD # | Requirement         | Alternatives                                                                      | Decision                                                                                               | Rationale                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ---- | ------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| MO-1 | Monitoring Service  | §Google Operations Suite

§Kyndryl-provide Monitoring solution (e.g ScienceLogic) | Google Operations Suite                                                                                | §Cloud-native monitoring services more easily integrated and deployed – integrated with GCP policy management and can be automatically installed via default policy settings

§Cloud native monitoring has greater visibility of cloud services than externally provided agents (especially for new cloud services or managed services that do not allow agents to be installed)

§Potential to be more cost effective as no requirement to purchase and manage third-party licenses, however costs must be closely managed                                                                                                                                                                                                                                                                   |
| MO-2 | Monitoring Agents   | §Google Ops Agent

§Kyndryl-provided agents                                       | Google Ops Agent (for OS)

Kyndryl-provided agents (if middleware or data base monitoring is required) | §Google Ops Agent provides a unified VM logging and monitoring agent that can be automatically installed and tracked – much simpler to manage for Kyndryl

§Cloud-native OS monitoring agent supported by Kyndryl and MCMS

§

§Kyndryl and MCMS will usually recommend installing additional agents, typically DataDog or ScienceLogic, if the managed services scope include monitoring of middleware or data bases                                                                                                                                                                                                                                                                                                                                                                         |
| MO-3 | Metrics Aggregation | §BigQuery

§Kyndryl MCMP AIOps                                                    | MCMP AIOps (basic)

BigQuery (if more advanced requirements)                                           | §MCMP AIOps Console is included in the base MCMS price

§As at Mar 2022, MCMP AIOps Console covers three uses cases:

1.Inventory (current includes everything – not filtered to match MCMS scope)

2.Events (from NetCool) and Tickets (from ServiceNow)

3.Day 2 Operations for basic Start / Stop / Resize operations (not currently integrated with ServiceNow for Change Management)

§MCMP AIOps does not currently pull in metrics from GCP (unlike Azure and AWS where it does pull metrics from Azure Monitor and AWS CloudWatch respectively) – as at Mar 2022

§

§For other uses cases that require retention of analysis of metrics the preferred approach would be to use the native GCP services:

‒Cloud Monitoring initially

‒Export to BigQuery for retention and analysis |
