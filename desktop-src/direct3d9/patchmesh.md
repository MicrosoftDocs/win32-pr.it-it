---
description: Definisce una mesh definita dalle patch di Bézier. La prima matrice è un elenco di vertici e la seconda matrice definisce le patch per la mesh mediante l'indicizzazione nella matrice di vertici.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcdefac9799736c796aef7cbb7222ab1942540d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520890"
---
# <a name="patchmesh"></a><span data-ttu-id="9e11f-104">PatchMesh</span><span class="sxs-lookup"><span data-stu-id="9e11f-104">PatchMesh</span></span>

<span data-ttu-id="9e11f-105">Definisce una mesh definita dalle patch di Bézier.</span><span class="sxs-lookup"><span data-stu-id="9e11f-105">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="9e11f-106">La prima matrice è un elenco di vertici e la seconda matrice definisce le patch per la mesh mediante l'indicizzazione nella matrice di vertici.</span><span class="sxs-lookup"><span data-stu-id="9e11f-106">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="9e11f-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="9e11f-107">Where:</span></span>

-   <span data-ttu-id="9e11f-108">nVertices: numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="9e11f-108">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="9e11f-109">vertici \[ nVertices \] : matrice di vertici.</span><span class="sxs-lookup"><span data-stu-id="9e11f-109">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="9e11f-110">Vedere [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="9e11f-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="9e11f-111">nPatches: numero di patch.</span><span class="sxs-lookup"><span data-stu-id="9e11f-111">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="9e11f-112">patch \[ nPatches \] : matrice di patch.</span><span class="sxs-lookup"><span data-stu-id="9e11f-112">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="9e11f-113">Vedere [**patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="9e11f-113">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="9e11f-114">\[ ... \] -È possibile usare qualsiasi modello di file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="9e11f-114">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="9e11f-115">Questa operazione rende l'architettura estendibile.</span><span class="sxs-lookup"><span data-stu-id="9e11f-115">This makes the architecture extensible.</span></span>

<span data-ttu-id="9e11f-116">Le patch usano i vertici nella matrice di vertici come punti di controllo per ogni patch.</span><span class="sxs-lookup"><span data-stu-id="9e11f-116">The patches use the vertices in the array of vertices as the control points for each patch.</span></span> <span data-ttu-id="9e11f-117">Si tratta di un modello legacy.</span><span class="sxs-lookup"><span data-stu-id="9e11f-117">This is a legacy template.</span></span> <span data-ttu-id="9e11f-118">Il modello mesh patch più recente è [**PatchMesh9**](patchmesh9.md).</span><span class="sxs-lookup"><span data-stu-id="9e11f-118">The latest patch mesh template is [**PatchMesh9**](patchmesh9.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9e11f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e11f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e11f-120">Modelli</span><span class="sxs-lookup"><span data-stu-id="9e11f-120">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



