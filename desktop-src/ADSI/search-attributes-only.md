---
title: Cerca solo attributi
description: A volte viene eseguita una ricerca per determinare il tipo di dati disponibile per un oggetto.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Cerca solo attributi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c2a97873dfb52f56b123919c3eedd277a63a74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955085"
---
# <a name="search-attributes-only"></a><span data-ttu-id="2b1eb-104">Cerca solo attributi</span><span class="sxs-lookup"><span data-stu-id="2b1eb-104">Search Attributes Only</span></span>

<span data-ttu-id="2b1eb-105">A volte viene eseguita una ricerca per determinare il tipo di dati disponibile per un oggetto.</span><span class="sxs-lookup"><span data-stu-id="2b1eb-105">Sometimes you perform a search to determine what type of data is available for an object.</span></span> <span data-ttu-id="2b1eb-106">In questo caso, si è interessati solo agli attributi e non ai valori dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2b1eb-106">In this case, you are interested only in the attributes, and not the values, of the object.</span></span> <span data-ttu-id="2b1eb-107">A tale scopo, è necessario impostare l'opzione "Cerca solo attributi".</span><span class="sxs-lookup"><span data-stu-id="2b1eb-107">To accomplish this, you set the "search attributes only" option.</span></span> <span data-ttu-id="2b1eb-108">Se si specifica questa opzione, vengono restituiti i nomi di attributo senza i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="2b1eb-108">Specifying this option returns the attribute names without their values.</span></span> <span data-ttu-id="2b1eb-109">Il set di risultati include tuttavia solo gli attributi a cui sono assegnati valori.</span><span class="sxs-lookup"><span data-stu-id="2b1eb-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="2b1eb-110">Si consideri, ad esempio, un oggetto con gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b1eb-110">For example, consider an object with the following attributes:</span></span>

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

<span data-ttu-id="2b1eb-111">Quando viene impostata l'opzione solo attributi di ricerca, il set di risultati include:</span><span class="sxs-lookup"><span data-stu-id="2b1eb-111">When the search attributes only option is set, the result set includes:</span></span>

``` syntax
First Name
Last Name
Phone Number
```

<span data-ttu-id="2b1eb-112">Per ulteriori informazioni sull'utilizzo dell'opzione solo attributi di ricerca con un'interfaccia di ricerca specifica, vedere:</span><span class="sxs-lookup"><span data-stu-id="2b1eb-112">For more information about using the search attributes only option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="2b1eb-113">Restituzione solo dei nomi di attributo con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="2b1eb-113">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)
-   [<span data-ttu-id="2b1eb-114">Ricerca con ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="2b1eb-114">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="2b1eb-115">Ricerca con OLE DB</span><span class="sxs-lookup"><span data-stu-id="2b1eb-115">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




