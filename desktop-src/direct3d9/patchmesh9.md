---
description: PatchMesh9 definisce una mesh definita dalle patch di Bézier, incluso un elenco di vertici e le patch per la mesh tramite l'indicizzazione nella matrice di vertici.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811e593117f2ec57a4718ea8078d96bcea87e71f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404704"
---
# <a name="patchmesh9"></a><span data-ttu-id="6dabd-103">PatchMesh9</span><span class="sxs-lookup"><span data-stu-id="6dabd-103">PatchMesh9</span></span>

<span data-ttu-id="6dabd-104">Definisce una mesh definita dalle patch di Bézier.</span><span class="sxs-lookup"><span data-stu-id="6dabd-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="6dabd-105">La prima matrice è un elenco di vertici e la seconda definisce le patch per la mesh tramite l'indicizzazione nella matrice dei vertici.</span><span class="sxs-lookup"><span data-stu-id="6dabd-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="6dabd-106">Dove:</span><span class="sxs-lookup"><span data-stu-id="6dabd-106">Where:</span></span>

-   <span data-ttu-id="6dabd-107">Tipo - Tipo di mesh patch: rettangolo, triangolo o N-patch.</span><span class="sxs-lookup"><span data-stu-id="6dabd-107">Type - Patch mesh type: rectangle, triangle, or N-patch.</span></span>
-   <span data-ttu-id="6dabd-108">Grado: grado delle variabili nell'equazione della curva.</span><span class="sxs-lookup"><span data-stu-id="6dabd-108">Degree - Degree of the variables in the curve equation.</span></span>
-   <span data-ttu-id="6dabd-109">Base: tipo di base di una superficie patch di ordine elevato.</span><span class="sxs-lookup"><span data-stu-id="6dabd-109">Basis - Basis type of a high-order patch surface.</span></span>
-   <span data-ttu-id="6dabd-110">nVertices : numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="6dabd-110">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="6dabd-111">vertices \[ nVertices \] - Matrice di vertici.</span><span class="sxs-lookup"><span data-stu-id="6dabd-111">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="6dabd-112">Vedere [**Vettore**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="6dabd-112">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="6dabd-113">nPatches : numero di patch.</span><span class="sxs-lookup"><span data-stu-id="6dabd-113">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="6dabd-114">patches \[ nPatches \] - Matrice di patch.</span><span class="sxs-lookup"><span data-stu-id="6dabd-114">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="6dabd-115">Vedere [**Patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="6dabd-115">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="6dabd-116">\[ ... \] - Qui è possibile usare qualsiasi modello di file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="6dabd-116">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="6dabd-117">In questo modo l'architettura è estensibile.</span><span class="sxs-lookup"><span data-stu-id="6dabd-117">This makes the architecture extensible.</span></span>

<span data-ttu-id="6dabd-118">Le patch usano i vertici nella matrice di vertici come punti di controllo per ogni patch.</span><span class="sxs-lookup"><span data-stu-id="6dabd-118">The patches use the vertices in the array of vertices as the control points for each patch.</span></span>

## <a name="see-also"></a><span data-ttu-id="6dabd-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6dabd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dabd-120">Modelli</span><span class="sxs-lookup"><span data-stu-id="6dabd-120">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



