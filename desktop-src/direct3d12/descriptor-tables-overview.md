---
title: Cenni preliminari sulle tabelle descrittori
description: Ogni tabella dei descrittori archivia i descrittori di uno o più tipi, ovvero SRVs, UAVe, CBVs e Samplers. Una tabella descrittore non è un'allocazione di memoria; è semplicemente un offset e una lunghezza in un heap del descrittore.
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d446a0570cf813eacaa4d036781e8cd4b8def3c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103578"
---
# <a name="descriptor-tables-overview"></a><span data-ttu-id="8e005-104">Cenni preliminari sulle tabelle descrittori</span><span class="sxs-lookup"><span data-stu-id="8e005-104">Descriptor Tables Overview</span></span>

<span data-ttu-id="8e005-105">Ogni tabella dei descrittori archivia i descrittori di uno o più tipi, ovvero SRVs, UAVe, CBVs e Samplers.</span><span class="sxs-lookup"><span data-stu-id="8e005-105">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="8e005-106">Una tabella descrittore non è un'allocazione di memoria; è semplicemente un offset e una lunghezza in un heap del descrittore.</span><span class="sxs-lookup"><span data-stu-id="8e005-106">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span>

-   [<span data-ttu-id="8e005-107">Riferimento a tabelle di descrittori</span><span class="sxs-lookup"><span data-stu-id="8e005-107">Referencing descriptor tables</span></span>](#referencing-descriptor-tables)
-   [<span data-ttu-id="8e005-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8e005-108">Related topics</span></span>](#related-topics)

## <a name="referencing-descriptor-tables"></a><span data-ttu-id="8e005-109">Riferimento a tabelle di descrittori</span><span class="sxs-lookup"><span data-stu-id="8e005-109">Referencing descriptor tables</span></span>

<span data-ttu-id="8e005-110">La pipeline grafica, tramite la firma radice, ottiene l'accesso alle risorse facendo riferimento a tabelle descrittore in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="8e005-110">The graphics pipeline, through the root signature, gain access to resources by referencing into descriptor tables by index.</span></span>

<span data-ttu-id="8e005-111">Una tabella dei descrittori è in realtà solo un intervallo secondario di un heap del descrittore.</span><span class="sxs-lookup"><span data-stu-id="8e005-111">A descriptor table is actually just a sub-range of a descriptor heap.</span></span> <span data-ttu-id="8e005-112">Gli heap del descrittore rappresentano l'allocazione di memoria sottostante per una raccolta di descrittori.</span><span class="sxs-lookup"><span data-stu-id="8e005-112">Descriptor heaps represent the underlying memory allocation for a collection of descriptors.</span></span> <span data-ttu-id="8e005-113">Poiché l'allocazione di memoria è una proprietà di un heap di descrittore, la definizione di una tabella del descrittore su uno di essi è garantita come l'identificazione di un'area nell'heap per l'hardware.</span><span class="sxs-lookup"><span data-stu-id="8e005-113">Since memory allocation is a property of a creating a descriptor heap, defining a descriptor table out of one is guaranteed to be as cheap as identifying a region in the heap to the hardware.</span></span> <span data-ttu-id="8e005-114">Le tabelle dei descrittori non devono essere create o distrutte a livello di API, ma sono semplicemente identificate come offset e le dimensioni di un heap ogni volta che vi si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="8e005-114">Descriptor tables don’t need to be created or destroyed at the API level– they are merely identified to drivers as an offset and size out of a heap whenever referenced.</span></span>

<span data-ttu-id="8e005-115">È certamente possibile che un'app definisca le tabelle dei descrittori di dimensioni molto grandi quando i relativi shader desiderano che la libertà di selezione da un vasto set di descrittori disponibili (spesso che fanno riferimento a trame) in tempo reale (probabilmente basati sui dati del materiale).</span><span class="sxs-lookup"><span data-stu-id="8e005-115">It is certainly possible for an app to define very large descriptor tables when its shaders want the freedom to select from a vast set of available descriptors (often referencing textures) on the fly (perhaps driven by material data).</span></span>

<span data-ttu-id="8e005-116">La firma radice fa riferimento alla voce della tabella descrittore con un riferimento all'heap, la posizione iniziale della tabella (un offset dall'inizio dell'heap) e la lunghezza (in voci) della tabella.</span><span class="sxs-lookup"><span data-stu-id="8e005-116">The Root Signature references the descriptor table entry with a reference to the heap, the start location of the table (an offset from the start of the heap), and the length (in entries) of the table.</span></span> <span data-ttu-id="8e005-117">Nell'immagine seguente vengono illustrati questi concetti: i puntatori alla tabella descrittore della firma radice e i descrittori all'interno dell'heap del descrittore che fanno riferimento alla trama completa o ai dati del buffer in un heap di caricamento.</span><span class="sxs-lookup"><span data-stu-id="8e005-117">The image below shows these concepts: the descriptor table pointers from the Root Signature and the descriptors within the descriptor heap referencing the full texture or buffer data in an upload heap.</span></span>

![tabelle descrittore](images/descriptor-table.png)

## <a name="related-topics"></a><span data-ttu-id="8e005-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8e005-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e005-120">Tabelle descrittore</span><span class="sxs-lookup"><span data-stu-id="8e005-120">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




