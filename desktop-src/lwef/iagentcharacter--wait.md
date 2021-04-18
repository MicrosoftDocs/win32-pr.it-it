---
title: IAgentCharacter attesa
description: IAgentCharacter attesa
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54ac2de03c78c220803a774537230938a00a776
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331412"
---
# <a name="iagentcharacterwait"></a><span data-ttu-id="c70f2-103">IAgentCharacter:: wait</span><span class="sxs-lookup"><span data-stu-id="c70f2-103">IAgentCharacter::Wait</span></span>

<span data-ttu-id="c70f2-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c70f2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="c70f2-105">Include la coda di animazione del carattere nell'animazione specificata (richiesta) finché non viene completata un'altra richiesta per un altro carattere.</span><span class="sxs-lookup"><span data-stu-id="c70f2-105">Holds the character's animation queue at the specified animation (request) until another request for another character completes.</span></span>

-   <span data-ttu-id="c70f2-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c70f2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c70f2-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="c70f2-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="c70f2-108">ID della richiesta da attendere.</span><span class="sxs-lookup"><span data-stu-id="c70f2-108">The ID of the request to wait for.</span></span>

</dd> <dt>

<span data-ttu-id="c70f2-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="c70f2-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="c70f2-110">Indirizzo di una variabile che riceve l'ID della richiesta di **attesa** .</span><span class="sxs-lookup"><span data-stu-id="c70f2-110">Address of a variable that receives the **Wait** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="c70f2-111">Usare questo metodo solo quando si supportano più caratteri (simultanei) e si vuole sequenziare l'interazione.</span><span class="sxs-lookup"><span data-stu-id="c70f2-111">Use this method only when you support multiple (simultaneous) characters and want to sequence their interaction.</span></span> <span data-ttu-id="c70f2-112">(Per un singolo carattere, ogni richiesta di animazione viene riprodotta in sequenza, dopo il completamento della richiesta precedente). Se si dispone di due caratteri e si desidera che la richiesta di animazione di un carattere attenda il completamento dell'animazione dell'altro carattere, impostare il metodo **wait** sull'ID richiesta di animazione dell'altro carattere.</span><span class="sxs-lookup"><span data-stu-id="c70f2-112">(For a single character, each animation request is played sequentially--after the previous request completes.) If you have two characters and want one character's animation request to wait until the other character's animation completes, set the **Wait** method to the other character's animation request ID.</span></span>

 

 




