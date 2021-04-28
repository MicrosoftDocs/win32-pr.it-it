---
description: "FaceAdjacency: viene creata un'istanza di questo modello per ogni mesh, che contiene informazioni sui vertici nella mesh duplicati l'uno dell'altro."
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0508b822f45c6796a793dc4b17caeaa1e30b4c3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090509"
---
# <a name="faceadjacency"></a><span data-ttu-id="508fa-103">FaceAdjacency</span><span class="sxs-lookup"><span data-stu-id="508fa-103">FaceAdjacency</span></span>

<span data-ttu-id="508fa-104">Viene creata un'istanza di questo modello per ogni mesh, che contiene informazioni sui vertici nella mesh duplicati l'uno dell'altro.</span><span class="sxs-lookup"><span data-stu-id="508fa-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="508fa-105">I duplicati vengono restituiti quando un vertice si trova su un gruppo di arrotondamento o un limite di materiale.</span><span class="sxs-lookup"><span data-stu-id="508fa-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="508fa-106">Lo scopo di questo modello è consentire al caricatore di determinare quali vertici che presentano parametri periferici diversi sono in realtà gli stessi vertici nel modello.</span><span class="sxs-lookup"><span data-stu-id="508fa-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="508fa-107">Alcune applicazioni ,ad esempio la semplificazione della mesh, possono usare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="508fa-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

<span data-ttu-id="508fa-108">Dove:</span><span class="sxs-lookup"><span data-stu-id="508fa-108">Where:</span></span>

-   <span data-ttu-id="508fa-109">nIndices : numero di indici nella mesh.</span><span class="sxs-lookup"><span data-stu-id="508fa-109">nIndices - Number of indices in the mesh.</span></span>
-   <span data-ttu-id="508fa-110">indici \[ nIndices \] : matrice di indici.</span><span class="sxs-lookup"><span data-stu-id="508fa-110">indices\[nIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="508fa-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="508fa-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="508fa-112">Modelli</span><span class="sxs-lookup"><span data-stu-id="508fa-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



