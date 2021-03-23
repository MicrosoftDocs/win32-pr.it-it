---
title: Utilizzo di tabelle descrittore
description: Le tabelle dei descrittori, ciascuna delle quali identifica un intervallo in un heap descrittore, vengono associate agli slot definiti dalla firma radice corrente in un elenco di comandi.
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104062"
---
# <a name="using-descriptor-tables"></a><span data-ttu-id="0f65f-103">Utilizzo di tabelle descrittore</span><span class="sxs-lookup"><span data-stu-id="0f65f-103">Using Descriptor Tables</span></span>

<span data-ttu-id="0f65f-104">Le tabelle dei descrittori, ciascuna delle quali identifica un intervallo in un heap descrittore, vengono associate agli slot definiti dalla firma radice corrente in un elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="0f65f-104">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span>

-   [<span data-ttu-id="0f65f-105">Indicizzazione di tabelle descrittore</span><span class="sxs-lookup"><span data-stu-id="0f65f-105">Indexing Descriptor Tables</span></span>](#indexing-descriptor-tables)
-   [<span data-ttu-id="0f65f-106">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f65f-106">Related topics</span></span>](#related-topics)

<span data-ttu-id="0f65f-107">Gli shader possono individuare le risorse a cui fanno riferimento i descrittori che compongono la tabella del descrittore.</span><span class="sxs-lookup"><span data-stu-id="0f65f-107">Shaders can locate resources referenced by the descriptors that make up the descriptor table.</span></span> <span data-ttu-id="0f65f-108">Altre associazioni di risorse: i buffer di indice, il buffer di vertex, i buffer di output del flusso, le destinazioni di rendering e lo stencil di profondità vengono eseguiti direttamente in un elenco di comandi anziché tramite descrittori.</span><span class="sxs-lookup"><span data-stu-id="0f65f-108">Other resource bindings - Index Buffers, Vertex Buffer, Stream Output Buffers, Render Targets, and Depth Stencil are done directly on a command list rather than via descriptors.</span></span> <span data-ttu-id="0f65f-109">Per concludere:</span><span class="sxs-lookup"><span data-stu-id="0f65f-109">To summarize:</span></span>

<span data-ttu-id="0f65f-110">I riferimenti alle risorse seguenti possono condividere la stessa tabella e l'heap del descrittore:</span><span class="sxs-lookup"><span data-stu-id="0f65f-110">The following resource references can share the same descriptor table and heap:</span></span>

-   <span data-ttu-id="0f65f-111">Viste delle risorse shader</span><span class="sxs-lookup"><span data-stu-id="0f65f-111">Shader resource views</span></span>
-   <span data-ttu-id="0f65f-112">Viste di accesso non ordinate</span><span class="sxs-lookup"><span data-stu-id="0f65f-112">Unordered access views</span></span>
-   <span data-ttu-id="0f65f-113">Viste del buffer costante</span><span class="sxs-lookup"><span data-stu-id="0f65f-113">Constant buffer views</span></span>

<span data-ttu-id="0f65f-114">I riferimenti alle risorse seguenti devono trovarsi nel proprio heap dei descrittori:</span><span class="sxs-lookup"><span data-stu-id="0f65f-114">The following resource references must be in their own descriptor heap:</span></span>

-   <span data-ttu-id="0f65f-115">Campionatori</span><span class="sxs-lookup"><span data-stu-id="0f65f-115">Samplers</span></span>

<span data-ttu-id="0f65f-116">Le risorse seguenti non vengono inserite nelle tabelle o negli heap del descrittore, ma vengono associate direttamente tramite gli elenchi di comandi:</span><span class="sxs-lookup"><span data-stu-id="0f65f-116">The following resources are not placed in descriptor tables or heaps, but are bound directly using command lists:</span></span>

-   <span data-ttu-id="0f65f-117">Index buffer</span><span class="sxs-lookup"><span data-stu-id="0f65f-117">Index buffers</span></span>
-   <span data-ttu-id="0f65f-118">Buffer vertici</span><span class="sxs-lookup"><span data-stu-id="0f65f-118">Vertex buffers</span></span>
-   <span data-ttu-id="0f65f-119">Buffer di output di flusso</span><span class="sxs-lookup"><span data-stu-id="0f65f-119">Stream output buffers</span></span>
-   <span data-ttu-id="0f65f-120">Destinazioni di rendering</span><span class="sxs-lookup"><span data-stu-id="0f65f-120">Render targets</span></span>
-   <span data-ttu-id="0f65f-121">Visualizzazioni stencil profondità</span><span class="sxs-lookup"><span data-stu-id="0f65f-121">Depth stencil views</span></span>

## <a name="indexing-descriptor-tables"></a><span data-ttu-id="0f65f-122">Indicizzazione di tabelle descrittore</span><span class="sxs-lookup"><span data-stu-id="0f65f-122">Indexing Descriptor Tables</span></span>

<span data-ttu-id="0f65f-123">Gli shader non possono eseguire l'indicizzazione dinamica tra i limiti della tabella descrittore da un determinato sito di chiamata nello shader.</span><span class="sxs-lookup"><span data-stu-id="0f65f-123">Shaders cannot dynamically index across descriptor table boundaries from a given call-site in the shader.</span></span> <span data-ttu-id="0f65f-124">Tuttavia, la selezione di un descrittore all'interno di una tabella descrittore può essere indicizzata dinamicamente nel codice dello shader all'interno di intervalli dello stesso tipo di descrittore, ad esempio l'indicizzazione in un'area contigua di SRVs.</span><span class="sxs-lookup"><span data-stu-id="0f65f-124">However, the selection of a descriptor within a descriptor table is allowed to be dynamically indexed in shader code within ranges of the same descriptor type (such as indexing across a contiguous region of SRVs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f65f-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f65f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f65f-126">Tabelle descrittore</span><span class="sxs-lookup"><span data-stu-id="0f65f-126">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




