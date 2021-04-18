---
description: Definisce una mesh definita dalle patch di Bézier. La prima matrice è un elenco di vertici e la seconda matrice definisce le patch per la mesh mediante l'indicizzazione nella matrice di vertici.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3d8232fe8c83358feb216acfb45a7877d7acb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304384"
---
# <a name="patchmesh9"></a><span data-ttu-id="89b5c-104">PatchMesh9</span><span class="sxs-lookup"><span data-stu-id="89b5c-104">PatchMesh9</span></span>

<span data-ttu-id="89b5c-105">Definisce una mesh definita dalle patch di Bézier.</span><span class="sxs-lookup"><span data-stu-id="89b5c-105">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="89b5c-106">La prima matrice è un elenco di vertici e la seconda matrice definisce le patch per la mesh mediante l'indicizzazione nella matrice di vertici.</span><span class="sxs-lookup"><span data-stu-id="89b5c-106">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

<span data-ttu-id="89b5c-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="89b5c-107">Where:</span></span>

-   <span data-ttu-id="89b5c-108">Type-patch mesh Type: Rectangle, Triangle o N-patch.</span><span class="sxs-lookup"><span data-stu-id="89b5c-108">Type - Patch mesh type: rectangle, triangle, or N-patch.</span></span>
-   <span data-ttu-id="89b5c-109">Grado di grado delle variabili nell'equazione della curva.</span><span class="sxs-lookup"><span data-stu-id="89b5c-109">Degree - Degree of the variables in the curve equation.</span></span>
-   <span data-ttu-id="89b5c-110">Base: tipo di base di una superficie di patch di ordine superiore.</span><span class="sxs-lookup"><span data-stu-id="89b5c-110">Basis - Basis type of a high-order patch surface.</span></span>
-   <span data-ttu-id="89b5c-111">nVertices: numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="89b5c-111">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="89b5c-112">vertici \[ nVertices \] : matrice di vertici.</span><span class="sxs-lookup"><span data-stu-id="89b5c-112">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="89b5c-113">Vedere [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="89b5c-113">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="89b5c-114">nPatches: numero di patch.</span><span class="sxs-lookup"><span data-stu-id="89b5c-114">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="89b5c-115">patch \[ nPatches \] : matrice di patch.</span><span class="sxs-lookup"><span data-stu-id="89b5c-115">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="89b5c-116">Vedere [**patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="89b5c-116">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="89b5c-117">\[ ... \] -È possibile usare qualsiasi modello di file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="89b5c-117">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="89b5c-118">Questa operazione rende l'architettura estendibile.</span><span class="sxs-lookup"><span data-stu-id="89b5c-118">This makes the architecture extensible.</span></span>

<span data-ttu-id="89b5c-119">Le patch usano i vertici nella matrice di vertici come punti di controllo per ogni patch.</span><span class="sxs-lookup"><span data-stu-id="89b5c-119">The patches use the vertices in the array of vertices as the control points for each patch.</span></span>

## <a name="see-also"></a><span data-ttu-id="89b5c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89b5c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b5c-121">Modelli</span><span class="sxs-lookup"><span data-stu-id="89b5c-121">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



