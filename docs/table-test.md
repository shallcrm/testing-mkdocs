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

| Column 1 | Column 2 | Column 3                                | Column 4               |
| -------- | -------- | --------------------------------------- | ---------------------- |
| Row 1    | Row 1    | \- bullet<br>\- bullet 2<br>\- bullet 3 | 1\. List<br>2\. List 2 |
| Row 2    | Row 2    | \- bullet                               | Text                   |
| Row 3    | Row 3    | Text                                    | Text                   |
| Row 4    | Row 4    | Text                                    | Text                   |