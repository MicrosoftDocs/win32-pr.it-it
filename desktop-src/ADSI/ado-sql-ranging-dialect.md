---
title: Sottolinguaggio ADO SQL
description: Quando si usa ADO (ActiveX Directory Objects), l'uso del sottolinguaggio SQL è necessario usare le virgolette singole (') per l'attributo e l'identificatore di intervallo.
ms.assetid: 0453aa9e-ed35-45ff-a728-e854bf0bb353
ms.tgt_platform: multiple
keywords:
- ADO SQL con dialetto ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f7b846cd3517613dd8ea914f53a7b31c30f8651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297709"
---
# <a name="ado-sql-ranging-dialect"></a><span data-ttu-id="45c82-104">Sottolinguaggio ADO SQL</span><span class="sxs-lookup"><span data-stu-id="45c82-104">ADO SQL Ranging Dialect</span></span>

<span data-ttu-id="45c82-105">Quando si usa ADO (ActiveX Directory Objects), l'uso del sottolinguaggio SQL è necessario usare le virgolette singole (') per l'attributo e l'identificatore di intervallo.</span><span class="sxs-lookup"><span data-stu-id="45c82-105">When using the ActiveX Directory Objects (ADO), using the SQL dialect, single quotation marks (') must be used around the attribute and range specifier.</span></span> <span data-ttu-id="45c82-106">Di seguito è riportato un esempio del dialetto ADO SQL.</span><span class="sxs-lookup"><span data-stu-id="45c82-106">The following is an example of the ADO SQL dialect.</span></span>


```sql
Command.CommandText = "select Name, 'member;Range=0-50' from 'LDAP://CN=Group1,DC=Fabrikam,DC=Com' where objectCategory='group'"
```



 

 




