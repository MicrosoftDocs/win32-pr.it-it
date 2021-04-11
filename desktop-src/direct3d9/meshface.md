---
description: Utilizzato dal modello mesh per definire i visi di una rete. Ogni elemento della matrice nFaceVertexIndices fa riferimento a un vertice mesh usato per compilare la faccia.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: MeshFace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9e8b73efb214f7a767d986830cccc83ee6cbc1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123444"
---
# <a name="meshface"></a><span data-ttu-id="099a0-104">MeshFace</span><span class="sxs-lookup"><span data-stu-id="099a0-104">MeshFace</span></span>

<span data-ttu-id="099a0-105">Utilizzato dal modello [**mesh**](mesh.md) per definire i visi di una rete.</span><span class="sxs-lookup"><span data-stu-id="099a0-105">Used by the [**Mesh**](mesh.md) template to define a mesh's faces.</span></span> <span data-ttu-id="099a0-106">Ogni elemento della matrice nFaceVertexIndices fa riferimento a un vertice mesh usato per compilare la faccia.</span><span class="sxs-lookup"><span data-stu-id="099a0-106">Each element of the nFaceVertexIndices array references a mesh vertex used to build the face.</span></span>

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

<span data-ttu-id="099a0-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="099a0-107">Where:</span></span>

-   <span data-ttu-id="099a0-108">nFaceVertexIndices: numero di indici.</span><span class="sxs-lookup"><span data-stu-id="099a0-108">nFaceVertexIndices - Number of indices.</span></span>
-   <span data-ttu-id="099a0-109">Array DWORD faceVertexIndices \[ nFaceVertexIndices \] -matrice di indici.</span><span class="sxs-lookup"><span data-stu-id="099a0-109">array DWORD faceVertexIndices\[nFaceVertexIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="099a0-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="099a0-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="099a0-111">Modelli</span><span class="sxs-lookup"><span data-stu-id="099a0-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



