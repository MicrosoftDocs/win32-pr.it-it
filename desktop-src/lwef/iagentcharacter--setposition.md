---
title: Posizione IAgentCharacter
description: Posizione IAgentCharacter
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044494"
---
# <a name="iagentcharactersetposition"></a><span data-ttu-id="8b141-103">IAgentCharacter:: seposition</span><span class="sxs-lookup"><span data-stu-id="8b141-103">IAgentCharacter::SetPosition</span></span>

<span data-ttu-id="8b141-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8b141-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

<span data-ttu-id="8b141-105">Imposta la posizione del frame di animazione del carattere.</span><span class="sxs-lookup"><span data-stu-id="8b141-105">Sets the position of the character's animation frame.</span></span>

-   <span data-ttu-id="8b141-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8b141-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8b141-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*</span><span class="sxs-lookup"><span data-stu-id="8b141-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*</span></span>
</dt> <dd>

<span data-ttu-id="8b141-108">Coordinata dello schermo del bordo sinistro del frame di animazione caratteri in pixel rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="8b141-108">Screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="8b141-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*</span><span class="sxs-lookup"><span data-stu-id="8b141-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*</span></span>
</dt> <dd>

<span data-ttu-id="8b141-110">Coordinata dello schermo del bordo superiore del frame di animazione caratteri in pixel rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="8b141-110">Screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="8b141-111">L'impostazione di questa proprietà si applica a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="8b141-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="8b141-112">Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sul relativo frame di animazione rettangolare.</span><span class="sxs-lookup"><span data-stu-id="8b141-112">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

> [!Note]  
> <span data-ttu-id="8b141-113">Diversamente dal metodo [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) , questa funzione non viene accodata.</span><span class="sxs-lookup"><span data-stu-id="8b141-113">Unlike the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) method, this function is not queued.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="8b141-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8b141-114">See Also</span></span>

[<span data-ttu-id="8b141-115">**IAgentCharacter:: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="8b141-115">**IAgentCharacter::GetPosition**</span></span>](iagentcharacter--getposition.md)


 

 




