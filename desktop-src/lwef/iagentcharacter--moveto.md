---
title: IAgentCharacter MoveTo
description: IAgentCharacter MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d1ba423dc637895216ff03e2adec2862bbf27d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046619"
---
# <a name="iagentcharactermoveto"></a><span data-ttu-id="82bac-103">IAgentCharacter:: MoveTo</span><span class="sxs-lookup"><span data-stu-id="82bac-103">IAgentCharacter::MoveTo</span></span>

<span data-ttu-id="82bac-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="82bac-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="82bac-105">Riproduce l'animazione dello stato di **spostamento** associato e sposta il frame di caratteri nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="82bac-105">Plays the associated **Moving** state animation and moves the character frame to the specified location.</span></span>

-   <span data-ttu-id="82bac-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="82bac-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="82bac-107">Quando la funzione restituisce, questa variabile contiene l'ID della richiesta.</span><span class="sxs-lookup"><span data-stu-id="82bac-107">When the function returns, this variable contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="82bac-108"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="82bac-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="82bac-109">Coordinata x della nuova posizione, espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="82bac-109">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="82bac-110">La posizione di un carattere è basata sull'angolo superiore sinistro del frame di animazione.</span><span class="sxs-lookup"><span data-stu-id="82bac-110">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="82bac-111"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="82bac-111"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="82bac-112">Coordinata y della nuova posizione, espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="82bac-112">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="82bac-113">La posizione di un carattere è basata sull'angolo superiore sinistro del frame di animazione.</span><span class="sxs-lookup"><span data-stu-id="82bac-113">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="82bac-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*</span><span class="sxs-lookup"><span data-stu-id="82bac-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="82bac-115">Parametro che specifica in millisecondi la velocità con cui viene spostato il frame del carattere.</span><span class="sxs-lookup"><span data-stu-id="82bac-115">A parameter specifying in milliseconds how quickly the character's frame moves.</span></span> <span data-ttu-id="82bac-116">Il valore consigliato è 1000.</span><span class="sxs-lookup"><span data-stu-id="82bac-116">The recommended value is 1000.</span></span> <span data-ttu-id="82bac-117">Se si specifica zero (0), il frame viene spostato senza riprodurre un'animazione.</span><span class="sxs-lookup"><span data-stu-id="82bac-117">Specifying zero (0) moves the frame without playing an animation.</span></span>

</dd> <dt>

<span data-ttu-id="82bac-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="82bac-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="82bac-119">Indirizzo di una variabile che riceve l'ID della richiesta [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) .</span><span class="sxs-lookup"><span data-stu-id="82bac-119">Address of a variable that receives the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="82bac-120">Quando si utilizza il protocollo HTTP per accedere ai dati di tipo carattere e animazione, utilizzare il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per garantire la disponibilità delle animazioni dello stato di **trasferimento** prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="82bac-120">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Moving** state animations before calling this method.</span></span> <span data-ttu-id="82bac-121">Anche se l'animazione non è caricata, il server sposta ancora il frame.</span><span class="sxs-lookup"><span data-stu-id="82bac-121">Even if the animation is not loaded, the server still moves the frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="82bac-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="82bac-122">See Also</span></span>

[<span data-ttu-id="82bac-123">**IAgentCharacter:: seposition**</span><span class="sxs-lookup"><span data-stu-id="82bac-123">**IAgentCharacter::SetPosition**</span></span>](iagentcharacter--setposition.md)


 

 