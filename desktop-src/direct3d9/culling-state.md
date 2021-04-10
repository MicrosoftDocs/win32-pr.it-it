---
description: Per migliorare le prestazioni di rendering, è possibile eliminare o rimuovere una primitiva che faccia parte della fotocamera.
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: Stato di eliminazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86e71fd7c6543f0d232e32a630d73e0ebbadae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127126"
---
# <a name="culling-state-direct3d-9"></a><span data-ttu-id="cd764-103">Stato di eliminazione (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cd764-103">Culling State (Direct3D 9)</span></span>

<span data-ttu-id="cd764-104">Per migliorare le prestazioni di rendering, è possibile eliminare o rimuovere una primitiva che faccia parte della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="cd764-104">To improve rendering performance, you can cull out (or remove) a primitive that faces away from the camera.</span></span> <span data-ttu-id="cd764-105">Per le primitive unilaterali, questo consente di risparmiare tempo di rendering perché un back-face non è visibile.</span><span class="sxs-lookup"><span data-stu-id="cd764-105">For single-sided primitives, this saves rendering time because a back-face is not visible.</span></span> <span data-ttu-id="cd764-106">Per abilitare l'eliminazione, è necessario conoscerne l'ordine di avvolgimento (in genere in senso antiorario).</span><span class="sxs-lookup"><span data-stu-id="cd764-106">To enable culling, you need to know the winding order of the vertices (typically counter-clockwise).</span></span> <span data-ttu-id="cd764-107">In questo esempio vengono rimosse tutte le primitive il cui retro è rivolto verso l'esterno (dato un ordine di avvolgimento in senso antiorario):</span><span class="sxs-lookup"><span data-stu-id="cd764-107">This example will remove any primitive whose back face is facing forward (given a counter-clockwise winding order):</span></span>


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a><span data-ttu-id="cd764-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cd764-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd764-109">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="cd764-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



