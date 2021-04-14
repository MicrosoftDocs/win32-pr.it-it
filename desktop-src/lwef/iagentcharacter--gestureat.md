---
title: IAgentCharacter GestureAt
description: IAgentCharacter GestureAt
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 266dc2d5e797ec0c7b30f7f827a094cd01c04195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396995"
---
# <a name="iagentcharactergestureat"></a><span data-ttu-id="7c5fb-103">IAgentCharacter::GestureAt</span><span class="sxs-lookup"><span data-stu-id="7c5fb-103">IAgentCharacter::GestureAt</span></span>

<span data-ttu-id="7c5fb-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7c5fb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="7c5fb-105">Riproduce l'animazione dello stato **gestuale** associato in base alla posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="7c5fb-105">Plays the associated **Gesturing** state animation based on the specified location.</span></span>

-   <span data-ttu-id="7c5fb-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7c5fb-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="7c5fb-107">Quando la funzione restituisce, *pdwReqID* contiene l'ID della richiesta.</span><span class="sxs-lookup"><span data-stu-id="7c5fb-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="7c5fb-108"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="7c5fb-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="7c5fb-109">Coordinata x della posizione specificata, espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="7c5fb-109">The x-coordinate of the specified location in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="7c5fb-110"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="7c5fb-110"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="7c5fb-111">Coordinata y della posizione specificata, espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="7c5fb-111">The y-coordinate of the specified location in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="7c5fb-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="7c5fb-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="7c5fb-113">Indirizzo di una variabile che riceve l'ID richiesta **GestureAt** .</span><span class="sxs-lookup"><span data-stu-id="7c5fb-113">Address of a variable that receives the **GestureAt** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="7c5fb-114">Il server determina automaticamente e riproduce l'animazione gestuale appropriata in base alla posizione corrente del carattere e alla posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="7c5fb-114">The server automatically determines and plays the appropriate gesturing animation based on the character's current position and the specified location.</span></span> <span data-ttu-id="7c5fb-115">Quando si usa il protocollo HTTP per accedere ai dati di tipo carattere e animazione, usare il metodo [**Prepare**](iagentcharacter--prepare.md) per assicurarsi che le animazioni siano disponibili prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="7c5fb-115">When using the HTTP protocol to access character and animation data, use the [**Prepare**](iagentcharacter--prepare.md) method to ensure that the animations are available before calling this method.</span></span>

 

 




