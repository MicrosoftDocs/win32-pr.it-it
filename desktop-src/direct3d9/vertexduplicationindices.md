---
description: Viene creata un'istanza di questo modello in base a mesh, che contiene informazioni sui vertici della mesh che sono duplicati l'uno dall'altro.
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d62278c206032c9a2dfed6ce9b2cd36c5e7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303673"
---
# <a name="vertexduplicationindices"></a><span data-ttu-id="ab224-103">VertexDuplicationIndices</span><span class="sxs-lookup"><span data-stu-id="ab224-103">VertexDuplicationIndices</span></span>

<span data-ttu-id="ab224-104">Viene creata un'istanza di questo modello in base a mesh, che contiene informazioni sui vertici della mesh che sono duplicati l'uno dall'altro.</span><span class="sxs-lookup"><span data-stu-id="ab224-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="ab224-105">Il risultato viene duplicato quando un vertice si trova su un gruppo o un limite di materiale smussato.</span><span class="sxs-lookup"><span data-stu-id="ab224-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="ab224-106">Lo scopo di questo modello è quello di consentire al caricatore di determinare i vertici che presentano parametri periferici diversi, in realtà gli stessi vertici del modello.</span><span class="sxs-lookup"><span data-stu-id="ab224-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="ab224-107">Alcune applicazioni (ad esempio, la semplificazione della rete) possono usare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="ab224-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

<span data-ttu-id="ab224-108">Dove:</span><span class="sxs-lookup"><span data-stu-id="ab224-108">Where:</span></span>

-   <span data-ttu-id="ab224-109">nIndices: numero di indici dei vertici.</span><span class="sxs-lookup"><span data-stu-id="ab224-109">nIndices - Number of vertex indices.</span></span> <span data-ttu-id="ab224-110">Il numero di vertici nella rete.</span><span class="sxs-lookup"><span data-stu-id="ab224-110">This is the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="ab224-111">nOriginalVertices: numero di vertici nella mesh prima che si verifichi la duplicazione.</span><span class="sxs-lookup"><span data-stu-id="ab224-111">nOriginalVertices - Number of vertices in the mesh before any duplication occurs.</span></span>
-   <span data-ttu-id="ab224-112">Gli indici di valore \[ n \] contengono l'indice dei vertici \[ per il vertice n \] nella matrice di vertici per la mesh se non si sono verificate duplicazioni.</span><span class="sxs-lookup"><span data-stu-id="ab224-112">The value indices\[n\] holds the vertex index that vertex\[n\] in the vertex array for the mesh would have had if no duplication had occurred.</span></span> <span data-ttu-id="ab224-113">Gli indici in questa matrice, pertanto, indicano i vertici duplicati.</span><span class="sxs-lookup"><span data-stu-id="ab224-113">Indices in this array that are the same, therefore, indicate duplicate vertices.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab224-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab224-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab224-115">Modelli</span><span class="sxs-lookup"><span data-stu-id="ab224-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



