---
title: IAgentCharacter GetPosition
description: IAgentCharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cdff0d6876fc7257e05014f3d9ba695db5d168
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332759"
---
# <a name="iagentcharactergetposition"></a><span data-ttu-id="86fe1-103">IAgentCharacter:: GetPosition</span><span class="sxs-lookup"><span data-stu-id="86fe1-103">IAgentCharacter::GetPosition</span></span>

<span data-ttu-id="86fe1-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="86fe1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

<span data-ttu-id="86fe1-105">Recupera la posizione del frame di animazione del carattere.</span><span class="sxs-lookup"><span data-stu-id="86fe1-105">Retrieves the character's animation frame position.</span></span>

-   <span data-ttu-id="86fe1-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="86fe1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="86fe1-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="86fe1-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="86fe1-108">Indirizzo di una variabile che riceve la coordinata dello schermo del bordo sinistro del frame di animazione caratteri in pixel rispetto all'origine della schermata (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="86fe1-108">Address of a variable that receives the screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="86fe1-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="86fe1-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="86fe1-110">Indirizzo di una variabile che riceve la coordinata dello schermo del bordo superiore del frame di animazione del carattere in pixel rispetto all'origine della schermata (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="86fe1-110">Address of a variable that receives the screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="86fe1-111">Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sul relativo frame di animazione rettangolare.</span><span class="sxs-lookup"><span data-stu-id="86fe1-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="86fe1-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="86fe1-112">See Also</span></span>

<span data-ttu-id="86fe1-113">[**IAgentCharacter:: seposition**](iagentcharacter--setposition.md), [ **IAgentCharacter:: GetSize**](iagentcharacter--getsize.md)</span><span class="sxs-lookup"><span data-stu-id="86fe1-113">[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md), [**IAgentCharacter::GetSize**](iagentcharacter--getsize.md)</span></span>


 

 




