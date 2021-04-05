---
title: Enumerazione
description: L'accesso e la manipolazione dei dati con ADSI fornisce diversi esempi di enumerazione. È inoltre possibile enumerare gli elementi figlio degli oggetti contenitore. Questi elementi figlio sono oggetti, anziché solo proprietà sugli oggetti.
ms.assetid: 1db19b00-8e43-4fc0-9099-1a1135219600
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, esempio di codice Visual Basic, uso di IADsContainer per enumerare gli oggetti
- contenitori ADSI, uso di IADsContainer per enumerare gli elementi figlio del contenitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ba90e86282939486b79ee09cd17352841e733e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955102"
---
# <a name="enumeration"></a><span data-ttu-id="8ca57-107">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="8ca57-107">Enumeration</span></span>

<span data-ttu-id="8ca57-108">[L'accesso e la manipolazione dei dati con ADSI](accessing-and-manipulating-data-with-adsi.md) fornisce diversi esempi di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="8ca57-108">[Accessing and Manipulating Data with ADSI](accessing-and-manipulating-data-with-adsi.md) provides several examples of enumeration.</span></span> <span data-ttu-id="8ca57-109">È inoltre possibile enumerare gli elementi figlio degli oggetti contenitore.</span><span class="sxs-lookup"><span data-stu-id="8ca57-109">You can also enumerate the children of container objects.</span></span> <span data-ttu-id="8ca57-110">Questi elementi figlio sono oggetti, anziché solo proprietà sugli oggetti.</span><span class="sxs-lookup"><span data-stu-id="8ca57-110">These children are objects themselves, rather than just properties on objects.</span></span>

<span data-ttu-id="8ca57-111">Nell'esempio seguente viene utilizzata l'interfaccia [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) per enumerare gli elementi figlio del contenitore.</span><span class="sxs-lookup"><span data-stu-id="8ca57-111">The following example uses the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface to enumerate the children of the container.</span></span>


```VB
Dim Container as IADsContainer
Dim Child as IADs

Set Container = GetObject("LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com")
 
For Each Child in Container
     Debug.Print Child.Name
Next Child
```



 

 




