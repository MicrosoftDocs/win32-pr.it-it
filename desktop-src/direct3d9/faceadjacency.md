---
description: Viene creata un'istanza di questo modello in base a mesh, che contiene informazioni sui vertici della mesh che sono duplicati l'uno dall'altro.
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2fd0f0b2bb328aa8b5ec39e7481c0b7fd766fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745570"
---
# <a name="faceadjacency"></a><span data-ttu-id="8d927-103">FaceAdjacency</span><span class="sxs-lookup"><span data-stu-id="8d927-103">FaceAdjacency</span></span>

<span data-ttu-id="8d927-104">Viene creata un'istanza di questo modello in base a mesh, che contiene informazioni sui vertici della mesh che sono duplicati l'uno dall'altro.</span><span class="sxs-lookup"><span data-stu-id="8d927-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="8d927-105">Il risultato viene duplicato quando un vertice si trova su un gruppo o un limite di materiale smussato.</span><span class="sxs-lookup"><span data-stu-id="8d927-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="8d927-106">Lo scopo di questo modello è quello di consentire al caricatore di determinare i vertici che presentano parametri periferici diversi, in realtà gli stessi vertici del modello.</span><span class="sxs-lookup"><span data-stu-id="8d927-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="8d927-107">Alcune applicazioni (ad esempio, la semplificazione della rete) possono usare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="8d927-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

<span data-ttu-id="8d927-108">Dove:</span><span class="sxs-lookup"><span data-stu-id="8d927-108">Where:</span></span>

-   <span data-ttu-id="8d927-109">nIndices: numero di indici nella rete.</span><span class="sxs-lookup"><span data-stu-id="8d927-109">nIndices - Number of indices in the mesh.</span></span>
-   <span data-ttu-id="8d927-110">indici \[ nIndices \] -matrice di indici.</span><span class="sxs-lookup"><span data-stu-id="8d927-110">indices\[nIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d927-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d927-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d927-112">Modelli</span><span class="sxs-lookup"><span data-stu-id="8d927-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



