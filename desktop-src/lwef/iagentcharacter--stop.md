---
title: Arresto IAgentCharacter
description: Arresto IAgentCharacter
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356c81996a9410eccb2007dc5261913e30a1b414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396491"
---
# <a name="iagentcharacterstop"></a><span data-ttu-id="55806-103">IAgentCharacter:: Stop</span><span class="sxs-lookup"><span data-stu-id="55806-103">IAgentCharacter::Stop</span></span>

<span data-ttu-id="55806-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="55806-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

<span data-ttu-id="55806-105">Arresta l'animazione specificata (richiesta) e la rimuove dalla coda di animazione del carattere.</span><span class="sxs-lookup"><span data-stu-id="55806-105">Stops the specified animation (request) and removes it from the character's animation queue.</span></span>

-   <span data-ttu-id="55806-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="55806-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="55806-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="55806-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="55806-108">ID della richiesta da arrestare.</span><span class="sxs-lookup"><span data-stu-id="55806-108">The ID of the request to stop.</span></span>

</dd> </dl>

<span data-ttu-id="55806-109">**Stop** può essere utilizzato anche per arrestare le chiamate di [**preparazione**](iagentcharacter--prepare.md) in coda.</span><span class="sxs-lookup"><span data-stu-id="55806-109">**Stop** can also be used to halt any queued [**Prepare**](iagentcharacter--prepare.md) calls.</span></span>

## <a name="see-also"></a><span data-ttu-id="55806-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="55806-110">See Also</span></span>

<span data-ttu-id="55806-111">[**IAgentCharacter::P repare**](iagentcharacter--prepare.md), [ **IAgentCharacter:: stopAll**](iagentcharacter--stopall.md)</span><span class="sxs-lookup"><span data-stu-id="55806-111">[**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md)</span></span>


 

 




