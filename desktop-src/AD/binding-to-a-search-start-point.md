---
title: Associazione al punto di inizio della ricerca
description: Il punto iniziale di una ricerca è un contenitore che contiene direttamente o indirettamente gli oggetti cercati.
ms.assetid: f93c1310-7c8b-4d28-bd4d-6fab969d3353
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, associazione a un punto di inizio della ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741986e651848c1d2a88ab016b63365db91b26b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470766"
---
# <a name="binding-to-the-search-start-point"></a><span data-ttu-id="697de-104">Associazione al punto di inizio della ricerca</span><span class="sxs-lookup"><span data-stu-id="697de-104">Binding to the Search Start Point</span></span>

<span data-ttu-id="697de-105">Il punto iniziale di una ricerca è un contenitore che contiene direttamente o indirettamente gli oggetti cercati.</span><span class="sxs-lookup"><span data-stu-id="697de-105">The start point for a search is a container that directly or indirectly contains the objects searched for.</span></span> <span data-ttu-id="697de-106">La ricerca non verrà eseguita nei contenitori sopra il punto di inizio della ricerca.</span><span class="sxs-lookup"><span data-stu-id="697de-106">The search will not be performed in containers above the search start point.</span></span> <span data-ttu-id="697de-107">Ad esempio, adottare la seguente struttura di directory ipotetica:</span><span class="sxs-lookup"><span data-stu-id="697de-107">For example, take the following hypothetical directory structure:</span></span>

``` syntax
Domain A
    Container 1
        Object 1
        Object 2
    Container 2
        Object 3
        Object 4
```

<span data-ttu-id="697de-108">Se viene eseguita una ricerca per tutti gli oggetti e il punto di inizio della ricerca è "container 2", verranno recuperati solo "Object 3" e "Object 4".</span><span class="sxs-lookup"><span data-stu-id="697de-108">If a search is performed for all objects and the search start point is "Container 2", only "Object 3" and "Object 4" would be retrieved.</span></span> <span data-ttu-id="697de-109">Se è stata eseguita la stessa ricerca con il punto di inizio della ricerca in "container 1", verranno recuperati "Object 1" e "Object 2".</span><span class="sxs-lookup"><span data-stu-id="697de-109">If the same search was performed with the search start point at "Container 1", "Object 1" and "Object 2" would be retrieved.</span></span>

<span data-ttu-id="697de-110">Per eseguire l'associazione al punto di inizio della ricerca, associare al ADsPath del contenitore che costituirà il punto di inizio della ricerca.</span><span class="sxs-lookup"><span data-stu-id="697de-110">To bind to the search start point, bind to the ADsPath of the container that will be the search start point.</span></span>

 

 




