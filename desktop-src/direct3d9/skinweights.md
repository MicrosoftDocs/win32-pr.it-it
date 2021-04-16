---
description: Viene creata un'istanza di questo modello in base alla rete.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759239a3a7ec8ebb608cf9ede6624105cee321b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520882"
---
# <a name="skinweights"></a><span data-ttu-id="0a0e0-103">SkinWeights</span><span class="sxs-lookup"><span data-stu-id="0a0e0-103">SkinWeights</span></span>

<span data-ttu-id="0a0e0-104">Viene creata un'istanza di questo modello in base alla rete.</span><span class="sxs-lookup"><span data-stu-id="0a0e0-104">This template is instantiated on a per-mesh basis.</span></span> <span data-ttu-id="0a0e0-105">All'interno di una mesh, viene visualizzata una sequenza di n istanze di questo modello, dove n è il numero di ossa (X file frame) che influenzano i vertici nella rete.</span><span class="sxs-lookup"><span data-stu-id="0a0e0-105">Within a mesh, a sequence of n instances of this template will appear, where n is the number of bones (X file frames) that influence the vertices in the mesh.</span></span> <span data-ttu-id="0a0e0-106">Ogni istanza del modello definisce fondamentalmente l'influenza di un particolare osso sulla rete.</span><span class="sxs-lookup"><span data-stu-id="0a0e0-106">Each instance of the template basically defines the influence of a particular bone on the mesh.</span></span> <span data-ttu-id="0a0e0-107">È presente un elenco di indici dei vertici e un elenco corrispondente di pesi.</span><span class="sxs-lookup"><span data-stu-id="0a0e0-107">There is a list of vertex indices, and a corresponding list of weights.</span></span>

``` syntax
template SkinWeights 
{ 
    < 6F0D123B-BAD2-4167-A0D0-80224F25FABB > 
    STRING transformNodeName; 
    DWORD nWeights; 
    array DWORD vertexIndices[nWeights]; 
    array float weights[nWeights]; 
    Matrix4x4 matrixOffset; 
} 
```

<span data-ttu-id="0a0e0-108">Dove:</span><span class="sxs-lookup"><span data-stu-id="0a0e0-108">Where:</span></span>

-   <span data-ttu-id="0a0e0-109">Il nome dell'osso la cui influenza viene definita è transformNodeName e nWeights è il numero di vertici interessati da questo osso.</span><span class="sxs-lookup"><span data-stu-id="0a0e0-109">The name of the bone whose influence is being defined is transformNodeName, and nWeights is the number of vertices affected by this bone.</span></span>
-   <span data-ttu-id="0a0e0-110">I vertici influenzati da questo osso sono contenuti in vertexIndices e i pesi per ogni vertice influenzato da questo osso sono contenuti in pesi.</span><span class="sxs-lookup"><span data-stu-id="0a0e0-110">The vertices influenced by this bone are contained in vertexIndices, and the weights for each of the vertices influenced by this bone are contained in weights.</span></span>
-   <span data-ttu-id="0a0e0-111">La matrice matrixOffset trasforma i vertici della mesh nello spazio dell'osso.</span><span class="sxs-lookup"><span data-stu-id="0a0e0-111">The matrix matrixOffset transforms the mesh vertices to the space of the bone.</span></span> <span data-ttu-id="0a0e0-112">Una volta concatenato alla trasformazione dell'osso, fornisce le coordinate dello spazio globale della mesh interessate dall'osso.</span><span class="sxs-lookup"><span data-stu-id="0a0e0-112">When concatenated to the bone's transform, this provides the world space coordinates of the mesh as affected by the bone.</span></span> <span data-ttu-id="0a0e0-113">Vedere [**Matrix4x4**](matrix4x4.md).</span><span class="sxs-lookup"><span data-stu-id="0a0e0-113">See [**Matrix4x4**](matrix4x4.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0a0e0-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a0e0-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a0e0-115">Modelli</span><span class="sxs-lookup"><span data-stu-id="0a0e0-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



