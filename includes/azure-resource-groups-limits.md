---
author: tfitzmac
ms.service: azure-resource-manager
ms.topic: include
ms.date: 08/19/2019	
ms.author: tomfitz
---
| Resource | Default limit | Maximum limit |
| --- | --- | --- |
| Resources per [resource group](../articles/azure-resource-manager/resource-group-overview.md#resource-groups), per resource type |800 |Some resource types can exceed the 800 limit. See [Resources not limited to 800 instances per resource group](../articles/azure-resource-manager/resources-without-rg-limit.md). |
| Deployments per resource group in the deployment history |800<sup>1</sup> |800 |
| Resources per deployment |800 |800 |
| Management locks per unique scope |20 |20 |
| Number of tags per resource or resource group |50 |50 |
| Tag key length |512 |512 |
| Tag value length |256 |256 |

<sup>1</sup>If you reach the limit of 800 deployments per resource group, delete deployments from the history that are no longer needed. Deleting an entry from the deployment history doesn't affect the deployed resources. For more information, see [Resolve error when deployment count exceeds 800](../articles/azure-resource-manager/deployment-quota-exceeded.md).

#### Template limits

| Value | Default limit | Maximum limit |
| --- | --- | --- |
| Parameters |256 |256 |
| Variables |256 |256 |
| Resources (including copy count) |800 |800 |
| Outputs |64 |64 |
| Template expression |24,576 chars |24,576 chars |
| Resources in exported templates |200 |200 | 
| Template size |4 MB |4 MB |
| Parameter file size |64 KB |64 KB |

You can exceed some template limits by using a nested template. For more information, see [Use linked templates when you deploy Azure resources](../articles/azure-resource-manager/resource-group-linked-templates.md). To reduce the number of parameters, variables, or outputs, you can combine several values into an object. For more information, see [Objects as parameters](../articles/azure-resource-manager/resource-manager-objects-as-parameters.md).
