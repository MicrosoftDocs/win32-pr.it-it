---
title: Ricerca di oggetti in base al nome
description: La maggior parte degli oggetti in Active Directory Domain Services utilizza la proprietà CN come attributo di denominazione.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo, ricerca, per nome
- ANNUNCIO oggetto, ricerca per nome
- Ricerca di oggetti in base al nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914faa443402a1d20698aabaf0bf4a112279a322
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707618"
---
# <a name="finding-objects-by-name"></a><span data-ttu-id="c63bb-106">Ricerca di oggetti in base al nome</span><span class="sxs-lookup"><span data-stu-id="c63bb-106">Finding Objects by Name</span></span>

<span data-ttu-id="c63bb-107">La maggior parte degli oggetti in Active Directory Domain Services utilizza la proprietà **CN** come attributo di denominazione.</span><span class="sxs-lookup"><span data-stu-id="c63bb-107">Most objects in Active Directory Domain Services use the **cn** property as their naming attribute.</span></span> <span data-ttu-id="c63bb-108">Alcuni oggetti, tuttavia, utilizzano un attributo di denominazione diverso da **CN**.</span><span class="sxs-lookup"><span data-stu-id="c63bb-108">Some objects, however, use a naming attribute other than **cn**.</span></span> <span data-ttu-id="c63bb-109">Un controller di dominio, ad esempio, usa la proprietà **domainDNS** per l'attributo Naming e un'unità organizzativa usa la proprietà **OrganizationalUnit** per l'attributo naming.</span><span class="sxs-lookup"><span data-stu-id="c63bb-109">For example, a domain controller uses the **domainDNS** property for the naming attribute and an organizational unit uses the **organizationalUnit** property for the naming attribute.</span></span> <span data-ttu-id="c63bb-110">Per evitare di dover utilizzare un attributo di denominazione diverso per diversi tipi di oggetto, è necessario utilizzare la proprietà **Name** , che contiene il nome distinto relativo dell'oggetto, per cercare gli oggetti in base al nome.</span><span class="sxs-lookup"><span data-stu-id="c63bb-110">To avoid having to use a different naming attribute for different object types, the **name** property, which contains the relative distinguished name of the object, should be used to search for objects by name.</span></span>

## <a name="examples"></a><span data-ttu-id="c63bb-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="c63bb-111">Examples</span></span>

<span data-ttu-id="c63bb-112">Negli esempi di codice riportati di seguito vengono illustrate stringhe di query diverse che possono essere utilizzate per trovare gli oggetti in base al nome.</span><span class="sxs-lookup"><span data-stu-id="c63bb-112">The following code examples show different query strings that can be used to find objects by name.</span></span>

<span data-ttu-id="c63bb-113">La stringa di query seguente consente di trovare tutti gli oggetti con un nome che inizia con "Jeff".</span><span class="sxs-lookup"><span data-stu-id="c63bb-113">The following query string finds all objects with a name that begins with "Jeff".</span></span>


```C++
(name=Jeff*)
```



<span data-ttu-id="c63bb-114">La stringa di query seguente consente di trovare tutti gli oggetti computer con un nome che inizia con "Leased" o "Corp".</span><span class="sxs-lookup"><span data-stu-id="c63bb-114">The following query string finds all computer objects with a name that begins with "leased" or "corp".</span></span>


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



<span data-ttu-id="c63bb-115">La stringa di query seguente consente di trovare tutti gli utenti e con un nome che inizia con "Karen" o "Jeff".</span><span class="sxs-lookup"><span data-stu-id="c63bb-115">The following query string finds all users and with a name that begins with "Karen" or "Jeff".</span></span>


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




