---
title: Dialetto ADO LDAP
description: Quando si usa ADO (ActiveX Directory Objects) con il dialetto LDAP, l'identificatore di attributo e di intervallo non richiede virgolette.
ms.assetid: adda9cf7-6588-48ee-85e2-fddbaf28807b
ms.tgt_platform: multiple
keywords:
- ADO LDAP con dialetto ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78dc2c7ff2dbfc81a76ff582145b7cf12916439
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855369"
---
# <a name="ado-ldap-ranging-dialect"></a><span data-ttu-id="d06b6-104">Dialetto ADO LDAP</span><span class="sxs-lookup"><span data-stu-id="d06b6-104">ADO LDAP Ranging Dialect</span></span>

<span data-ttu-id="d06b6-105">Quando si usa ADO (ActiveX Directory Objects) con il dialetto LDAP, l'identificatore di attributo e di intervallo non richiede virgolette.</span><span class="sxs-lookup"><span data-stu-id="d06b6-105">When using ActiveX Directory Objects (ADO) with the LDAP dialect, the attribute and range specifier do not require quotation marks.</span></span>

<span data-ttu-id="d06b6-106">Di seguito è riportato un esempio del dialetto LDAP ADO.</span><span class="sxs-lookup"><span data-stu-id="d06b6-106">The following is an example of the ADO LDAP dialect.</span></span>


```C++
Command.Text = "<LDAP://CN=NewGroup,DC=Fabrikam,DC=Com>;(objectCategory=group);name,member;Range=51-*;base"
```



 

 




