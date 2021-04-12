---
description: L'interpolazione di vertici combina due posizioni fornite dall'utente (o normali).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Interpolazione di vertici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a5458e384fa69b91b1eab1623fb526d514591f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225419"
---
# <a name="vertex-tweening-direct3d-9"></a><span data-ttu-id="87e81-103">Interpolazione di vertici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="87e81-103">Vertex Tweening (Direct3D 9)</span></span>

<span data-ttu-id="87e81-104">L'interpolazione di vertici combina due posizioni fornite dall'utente (o normali).</span><span class="sxs-lookup"><span data-stu-id="87e81-104">Vertex tweening blends two user-provided positions (or normals).</span></span> <span data-ttu-id="87e81-105">L'interpolazione si escludono a vicenda dalla fusione dei vertici con pesi.</span><span class="sxs-lookup"><span data-stu-id="87e81-105">Tweening is mutually exclusive from vertex blending with weights.</span></span> <span data-ttu-id="87e81-106">L'interpolazione viene eseguita prima dell'illuminazione e del ritaglio ed è abilitata impostando D3DRS \_ VERTEXBLEND su D3DVBF \_ tweening.</span><span class="sxs-lookup"><span data-stu-id="87e81-106">Tweening is performed before lighting and clipping, and is enabled by setting D3DRS\_VERTEXBLEND to D3DVBF\_TWEENING.</span></span> <span data-ttu-id="87e81-107">La posizione del vertice risultante viene calcolata in base a quanto segue:</span><span class="sxs-lookup"><span data-stu-id="87e81-107">The resulting vertex position is computed by:</span></span>


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



<span data-ttu-id="87e81-108">Lo stesso approccio viene usato per il calcolo delle normali.</span><span class="sxs-lookup"><span data-stu-id="87e81-108">The same approach is used for calculating normals.</span></span> <span data-ttu-id="87e81-109">Per altre informazioni, vedere [using Vertex Tweening (Direct3D 9)](using-vertex-tweening.md).</span><span class="sxs-lookup"><span data-stu-id="87e81-109">For more information, see [Using Vertex Tweening (Direct3D 9)](using-vertex-tweening.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="87e81-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87e81-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87e81-111">Blending Geometry</span><span class="sxs-lookup"><span data-stu-id="87e81-111">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



