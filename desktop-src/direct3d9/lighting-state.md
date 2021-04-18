---
description: Se non si fa luce con un vertex shader o una pixel shader, è possibile scegliere di usare il motore di illuminazione nel Runtime.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Stato illuminazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f0e7b7ec4a8bcf0ee27c9bc1e643536819d8fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303724"
---
# <a name="lighting-state-direct3d-9"></a><span data-ttu-id="759da-103">Stato illuminazione (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="759da-103">Lighting State (Direct3D 9)</span></span>

<span data-ttu-id="759da-104">Se non si fa luce con un vertex shader o una pixel shader, è possibile scegliere di usare il motore di illuminazione nel Runtime.</span><span class="sxs-lookup"><span data-stu-id="759da-104">If you do not light with a vertex shader or a pixel shader, you may choose to use the lighting engine in the runtime.</span></span> <span data-ttu-id="759da-105">Il motore di illuminazione richiede che i dati dei vertici contengano normali per ogni vertice; i vertici senza dati normali genereranno un prodotto a virgola pari a zero in tutti i calcoli di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="759da-105">The lighting engine requires that the vertex data contains per-vertex normals; vertices without normal data will generate a dot product of zero in all lighting computations.</span></span> <span data-ttu-id="759da-106">I calcoli di illuminazione sono trattati in modo più dettagliato in [matematica di illuminazione (Direct3D 9)](mathematics-of-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="759da-106">The lighting calculations are covered in more detail in [Mathematics of Lighting (Direct3D 9)](mathematics-of-lighting.md).</span></span>

<span data-ttu-id="759da-107">Per abilitare il motore di illuminazione, usare:</span><span class="sxs-lookup"><span data-stu-id="759da-107">To enable the lighting engine, use:</span></span>


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a><span data-ttu-id="759da-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="759da-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="759da-109">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="759da-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



