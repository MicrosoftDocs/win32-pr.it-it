---
title: Recupero delle informazioni del catalogo
description: Recupero delle informazioni del catalogo
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Windows Media Player Online Stores, recupero delle informazioni del catalogo
- archivi online, recupero delle informazioni del catalogo
- digitare 1 archivi online, recupero delle informazioni del catalogo
- Windows Media Player Online Stores, informazioni di diagnostica sui cataloghi
- archivi online, informazioni di diagnostica sui cataloghi
- digitare 1 negozi online, informazioni di diagnostica sui cataloghi
- Windows Media Player Online Stores, catcomp.exe
- archivi online, catcomp.exe
- digitare 1 Store online, catcomp.exe
- catcomp.exe
- informazioni di diagnostica sui cataloghi
- recupero delle informazioni del catalogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721d6ba3e4d6b5106cf44446d4c96ed842ccd61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712727"
---
# <a name="retrieving-catalog-information"></a><span data-ttu-id="b395d-115">Recupero delle informazioni del catalogo</span><span class="sxs-lookup"><span data-stu-id="b395d-115">Retrieving Catalog Information</span></span>

<span data-ttu-id="b395d-116">È possibile visualizzare le informazioni di diagnostica su un catalogo eseguendo catcomp con la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="b395d-116">You can display diagnostic information on a catalog by running catcomp with the following syntax:</span></span>


```C++
catcomp info <catalogpath> [track|artist|album] [ID]
```



<span data-ttu-id="b395d-117">Ad esempio, il comando seguente Visualizza le informazioni su un intero catalogo, incluse la versione, le impostazioni locali e le informazioni interne sugli elementi del catalogo:</span><span class="sxs-lookup"><span data-stu-id="b395d-117">For example, the following command displays information on an entire catalog, including the version, locale, and internal information on catalog items:</span></span>


```C++
catcomp info C:\Catalog210\catalog.wmdb
```



<span data-ttu-id="b395d-118">Di seguito vengono visualizzate le informazioni per la traccia con ID 3256:</span><span class="sxs-lookup"><span data-stu-id="b395d-118">The following displays information for the track with ID 3256:</span></span>


```C++
catcomp info C:\Catalog210\catalog.wmdb track 3256
```



 

 




