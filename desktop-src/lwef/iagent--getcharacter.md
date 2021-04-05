---
title: IAgent getcharacter
description: IAgent getcharacter
ms.assetid: c54e3aa3-49ea-475c-831c-03865438e1d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4653d15c4c0f7143fcc3087f7c5d9f0d3212b8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855986"
---
# <a name="iagentgetcharacter"></a><span data-ttu-id="d3089-103">IAgent:: getcharacter</span><span class="sxs-lookup"><span data-stu-id="d3089-103">IAgent::GetCharacter</span></span>

<span data-ttu-id="d3089-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d3089-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCharacter(
   long dwCharID  // character ID
);
```

<span data-ttu-id="d3089-105">Recupera [**IAgentCharacter**](iagentcharacter.md) per un carattere caricato.</span><span class="sxs-lookup"><span data-stu-id="d3089-105">Retrieves the [**IAgentCharacter**](iagentcharacter.md) for a loaded character.</span></span>

-   <span data-ttu-id="d3089-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d3089-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d3089-107"><span id="DwCharID_"></span><span id="dwcharid_"></span><span id="DWCHARID_"></span>*DwCharID*</span><span class="sxs-lookup"><span data-stu-id="d3089-107"><span id="DwCharID_"></span><span id="dwcharid_"></span><span id="DWCHARID_"></span>*DwCharID*</span></span> 
</dt> <dd>

<span data-ttu-id="d3089-108">ID del carattere.</span><span class="sxs-lookup"><span data-stu-id="d3089-108">The character's ID.</span></span>

</dd> </dl>

 

 




