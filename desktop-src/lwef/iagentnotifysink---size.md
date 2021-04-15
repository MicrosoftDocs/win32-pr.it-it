---
title: Dimensioni IAgentNotifySink
description: Dimensioni IAgentNotifySink
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515907"
---
# <a name="iagentnotifysinksize"></a><span data-ttu-id="47ebc-103">IAgentNotifySink:: size</span><span class="sxs-lookup"><span data-stu-id="47ebc-103">IAgentNotifySink::Size</span></span>

<span data-ttu-id="47ebc-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="47ebc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

<span data-ttu-id="47ebc-105">Notifica a un'applicazione client quando il carattere è stato ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="47ebc-105">Notifies a client application when the character has been resized.</span></span>

-   <span data-ttu-id="47ebc-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="47ebc-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="47ebc-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="47ebc-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="47ebc-108">Identificatore del carattere che è stato ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="47ebc-108">Identifier of the character that has been resized.</span></span>

</dd> <dt>

<span data-ttu-id="47ebc-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span><span class="sxs-lookup"><span data-stu-id="47ebc-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="47ebc-110">Larghezza del fotogramma di animazione del carattere in pixel.</span><span class="sxs-lookup"><span data-stu-id="47ebc-110">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="47ebc-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span><span class="sxs-lookup"><span data-stu-id="47ebc-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="47ebc-112">Altezza del frame di animazione del carattere in pixel.</span><span class="sxs-lookup"><span data-stu-id="47ebc-112">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="47ebc-113">Questo evento viene inviato a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="47ebc-113">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="47ebc-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="47ebc-114">See Also</span></span>

<span data-ttu-id="47ebc-115">[**IAgentCharacter:: GetSize**](iagentcharacter--getsize.md), [ **IAgentCharacter:: sesize**](iagentcharacter--setsize.md)</span><span class="sxs-lookup"><span data-stu-id="47ebc-115">[**IAgentCharacter::GetSize**](iagentcharacter--getsize.md), [**IAgentCharacter::SetSize**](iagentcharacter--setsize.md)</span></span>


 

 




