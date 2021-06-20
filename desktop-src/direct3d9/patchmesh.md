---
description: PatchMesh definisce una mesh definita dalle patch di Bézier, incluso un elenco di vertici e le patch per la mesh tramite l'indicizzazione nella matrice dei vertici.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabb3846246c7fb76a7146baf0b30bd9730fe24b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404714"
---
# <a name="patchmesh"></a><span data-ttu-id="82d04-103">PatchMesh</span><span class="sxs-lookup"><span data-stu-id="82d04-103">PatchMesh</span></span>

<span data-ttu-id="82d04-104">Definisce una mesh definita dalle patch di Bézier.</span><span class="sxs-lookup"><span data-stu-id="82d04-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="82d04-105">La prima matrice è un elenco di vertici e la seconda matrice definisce le patch per la mesh tramite l'indicizzazione nella matrice dei vertici.</span><span class="sxs-lookup"><span data-stu-id="82d04-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

``` syntax
template PatchMesh
{
    < D02C95CC-EDBA-4305-9B5D-1820D7704BBF >
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
}
```

<span data-ttu-id="82d04-106">Dove:</span><span class="sxs-lookup"><span data-stu-id="82d04-106">Where:</span></span>

-   <span data-ttu-id="82d04-107">nVertices: numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="82d04-107">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="82d04-108">vertices \[ nVertices \] : matrice di vertici.</span><span class="sxs-lookup"><span data-stu-id="82d04-108">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="82d04-109">Vedere [**Vector.**](vector.md)</span><span class="sxs-lookup"><span data-stu-id="82d04-109">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="82d04-110">nPatches: numero di patch.</span><span class="sxs-lookup"><span data-stu-id="82d04-110">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="82d04-111">patches \[ nPatches \] : matrice di patch.</span><span class="sxs-lookup"><span data-stu-id="82d04-111">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="82d04-112">Vedere [**Patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="82d04-112">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="82d04-113">\[ ... \] - Qui è possibile usare qualsiasi modello di file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="82d04-113">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="82d04-114">In questo modo l'architettura è estensibile.</span><span class="sxs-lookup"><span data-stu-id="82d04-114">This makes the architecture extensible.</span></span>

<span data-ttu-id="82d04-115">Le patch usano i vertici nella matrice di vertici come punti di controllo per ogni patch.</span><span class="sxs-lookup"><span data-stu-id="82d04-115">The patches use the vertices in the array of vertices as the control points for each patch.</span></span> <span data-ttu-id="82d04-116">Si tratta di un modello legacy.</span><span class="sxs-lookup"><span data-stu-id="82d04-116">This is a legacy template.</span></span> <span data-ttu-id="82d04-117">Il modello patch mesh più recente è [**PatchMesh9.**](patchmesh9.md)</span><span class="sxs-lookup"><span data-stu-id="82d04-117">The latest patch mesh template is [**PatchMesh9**](patchmesh9.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="82d04-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82d04-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d04-119">Modelli</span><span class="sxs-lookup"><span data-stu-id="82d04-119">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



