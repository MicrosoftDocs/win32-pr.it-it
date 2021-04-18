---
description: Membri di CMSPCallMultiGraph
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: Membri di CMSPCallMultiGraph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312722"
---
# <a name="cmspcallmultigraph-members"></a><span data-ttu-id="39113-103">Membri di CMSPCallMultiGraph</span><span class="sxs-lookup"><span data-stu-id="39113-103">CMSPCallMultiGraph Members</span></span>

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

<span data-ttu-id="39113-104">I blocchi di attesa archiviano le informazioni relative all'attesa registrata nel pool di thread.</span><span class="sxs-lookup"><span data-stu-id="39113-104">The wait blocks store the information about the wait registered to the thread pool.</span></span> <span data-ttu-id="39113-105">Include gli handle di attesa restituiti dalla chiamata [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) e un puntatore alla struttura del contesto.</span><span class="sxs-lookup"><span data-stu-id="39113-105">It includes the wait handles returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) call and a pointer to the context structure.</span></span> <span data-ttu-id="39113-106">Ogni blocco nella matrice è per un grafico in uno degli oggetti flusso.</span><span class="sxs-lookup"><span data-stu-id="39113-106">Each block in the array is for a graph in one of the stream objects.</span></span> <span data-ttu-id="39113-107">L'offset di un blocco in questa matrice è uguale all'offset del flusso proprietario del grafico.</span><span class="sxs-lookup"><span data-stu-id="39113-107">The offset of a block in this array is the same as the offset of the stream that owns the graph.</span></span>

 

 
