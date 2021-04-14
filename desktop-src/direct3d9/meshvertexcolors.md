---
description: Specifica i colori dei vertici per una mesh, anziché applicare un materiale per volto o per mesh.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: MeshVertexColors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba55d601b29e0962c5d56e86ae052c454bf3adc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401136"
---
# <a name="meshvertexcolors"></a><span data-ttu-id="6e2d9-103">MeshVertexColors</span><span class="sxs-lookup"><span data-stu-id="6e2d9-103">MeshVertexColors</span></span>

<span data-ttu-id="6e2d9-104">Specifica i colori dei vertici per una mesh, anziché applicare un materiale per volto o per mesh.</span><span class="sxs-lookup"><span data-stu-id="6e2d9-104">Specifies vertex colors for a mesh, instead of applying a material per face or per mesh.</span></span>

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

<span data-ttu-id="6e2d9-105">Dove:</span><span class="sxs-lookup"><span data-stu-id="6e2d9-105">Where:</span></span>

-   <span data-ttu-id="6e2d9-106">nVertexColors: numero di colori.</span><span class="sxs-lookup"><span data-stu-id="6e2d9-106">nVertexColors - Number of colors.</span></span> <span data-ttu-id="6e2d9-107">Corrisponde al numero di vertici nella rete.</span><span class="sxs-lookup"><span data-stu-id="6e2d9-107">This matches the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="6e2d9-108">Array IndexColor vertexColors \[ nVertexColors \] -matrice di colori indicizzati.</span><span class="sxs-lookup"><span data-stu-id="6e2d9-108">array IndexColor vertexColors\[nVertexColors\] - Array of indexed colors.</span></span> <span data-ttu-id="6e2d9-109">Vedere [**IndexedColor**](indexedcolor.md).</span><span class="sxs-lookup"><span data-stu-id="6e2d9-109">See [**IndexedColor**](indexedcolor.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6e2d9-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e2d9-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e2d9-111">Modelli</span><span class="sxs-lookup"><span data-stu-id="6e2d9-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



