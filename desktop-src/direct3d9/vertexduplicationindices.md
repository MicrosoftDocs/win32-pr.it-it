---
description: "VertexDuplicationIndices: viene creata un'istanza di questo modello per ogni mesh, che contiene informazioni sui vertici nella mesh duplicati l'uno dell'altro."
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b33a8c5fca4f479eec6e9864d4528d4e3e4a1e32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090179"
---
# <a name="vertexduplicationindices"></a><span data-ttu-id="5fa3e-103">VertexDuplicationIndices</span><span class="sxs-lookup"><span data-stu-id="5fa3e-103">VertexDuplicationIndices</span></span>

<span data-ttu-id="5fa3e-104">Viene creata un'istanza di questo modello per ogni mesh, che contiene informazioni sui vertici nella mesh duplicati l'uno dell'altro.</span><span class="sxs-lookup"><span data-stu-id="5fa3e-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="5fa3e-105">I duplicati si verificano quando un vertice si trova su un gruppo di smussamento o un limite materiale.</span><span class="sxs-lookup"><span data-stu-id="5fa3e-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="5fa3e-106">Lo scopo di questo modello è consentire al caricatore di determinare quali vertici che presentano parametri periferici diversi sono effettivamente gli stessi vertici nel modello.</span><span class="sxs-lookup"><span data-stu-id="5fa3e-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="5fa3e-107">Alcune applicazioni ,ad esempio la semplificazione della mesh, possono usare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="5fa3e-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

<span data-ttu-id="5fa3e-108">Dove:</span><span class="sxs-lookup"><span data-stu-id="5fa3e-108">Where:</span></span>

-   <span data-ttu-id="5fa3e-109">nIndices: numero di indici dei vertici.</span><span class="sxs-lookup"><span data-stu-id="5fa3e-109">nIndices - Number of vertex indices.</span></span> <span data-ttu-id="5fa3e-110">Questo è il numero di vertici nella mesh.</span><span class="sxs-lookup"><span data-stu-id="5fa3e-110">This is the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="5fa3e-111">nOriginalVertices: numero di vertici nella mesh prima che si verifichi qualsiasi duplicazione.</span><span class="sxs-lookup"><span data-stu-id="5fa3e-111">nOriginalVertices - Number of vertices in the mesh before any duplication occurs.</span></span>
-   <span data-ttu-id="5fa3e-112">Gli indici di valore n contiene l'indice dei vertici che il vertice n nella matrice dei vertici per la mesh avrebbe avuto se non fosse stata \[ \] \[ \] verificata alcuna duplicazione.</span><span class="sxs-lookup"><span data-stu-id="5fa3e-112">The value indices\[n\] holds the vertex index that vertex\[n\] in the vertex array for the mesh would have had if no duplication had occurred.</span></span> <span data-ttu-id="5fa3e-113">Gli indici in questa matrice che sono gli stessi, pertanto, indicano vertici duplicati.</span><span class="sxs-lookup"><span data-stu-id="5fa3e-113">Indices in this array that are the same, therefore, indicate duplicate vertices.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fa3e-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fa3e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fa3e-115">Modelli</span><span class="sxs-lookup"><span data-stu-id="5fa3e-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



