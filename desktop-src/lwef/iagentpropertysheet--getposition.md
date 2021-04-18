---
title: IAgentPropertySheet GetPosition
description: IAgentPropertySheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298327"
---
# <a name="iagentpropertysheetgetposition"></a><span data-ttu-id="14529-103">IAgentPropertySheet:: GetPosition</span><span class="sxs-lookup"><span data-stu-id="14529-103">IAgentPropertySheet::GetPosition</span></span>

<span data-ttu-id="14529-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="14529-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

<span data-ttu-id="14529-105">Recupera la posizione della finestra delle proprietà dell'agente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="14529-105">Retrieves the Microsoft Agent's property sheet window position.</span></span>

-   <span data-ttu-id="14529-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="14529-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="14529-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="14529-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="14529-108">Indirizzo di una variabile che riceve la coordinata dello schermo del bordo sinistro della finestra delle proprietà, espressa in pixel, rispetto all'origine della schermata (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="14529-108">Address of a variable that receives the screen coordinate of the left edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="14529-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="14529-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="14529-110">Indirizzo di una variabile che riceve la coordinata dello schermo del bordo superiore della finestra delle proprietà in pixel, rispetto all'origine della schermata (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="14529-110">Address of a variable that receives the screen coordinate of the top edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="14529-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="14529-111">See Also</span></span>

[<span data-ttu-id="14529-112">**IAgentPropertySheet:: GetSize**</span><span class="sxs-lookup"><span data-stu-id="14529-112">**IAgentPropertySheet::GetSize**</span></span>](iagentpropertysheet--getsize.md)


 

 




