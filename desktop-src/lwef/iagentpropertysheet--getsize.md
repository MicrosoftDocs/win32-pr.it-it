---
title: IAgentPropertySheet GetSize
description: IAgentPropertySheet GetSize
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5e185a6e8d55d87e561f727c8dc9df8a8cfd63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298326"
---
# <a name="iagentpropertysheetgetsize"></a><span data-ttu-id="51806-103">IAgentPropertySheet:: GetSize</span><span class="sxs-lookup"><span data-stu-id="51806-103">IAgentPropertySheet::GetSize</span></span>

<span data-ttu-id="51806-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51806-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

<span data-ttu-id="51806-105">Recupera le dimensioni della finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="51806-105">Retrieves the size of the Microsoft Agent property sheet window.</span></span>

-   <span data-ttu-id="51806-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="51806-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="51806-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="51806-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="51806-108">Indirizzo di una variabile che riceve la larghezza della finestra delle proprietà in pixel rispetto all'origine della schermata (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="51806-108">Address of a variable that receives the width of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="51806-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="51806-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="51806-110">Indirizzo di una variabile che riceve l'altezza della finestra delle proprietà in pixel rispetto all'origine della schermata (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="51806-110">Address of a variable that receives the height of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="51806-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="51806-111">See Also</span></span>

[<span data-ttu-id="51806-112">**IAgentPropertySheet:: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="51806-112">**IAgentPropertySheet::GetPosition**</span></span>](iagentpropertysheet--getposition.md)


 

 




