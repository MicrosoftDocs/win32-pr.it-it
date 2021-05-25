---
title: Heap dei descrittori non visibili allo shader
description: Gli shader non possono fare riferimento ad alcuni heap dei descrittori tramite tabelle di descrittori, ma esistono per aiutare l'app a eseguire lo staging dei descrittori prima di registrare un elenco di comandi o perché non è necessario alcun heap visibile allo shader.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51d30c7a99250ee0842b79d76ccebb6150bcf9a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343456"
---
# <a name="non-shader-visible-descriptor-heaps"></a><span data-ttu-id="2f194-103">Heap dei descrittori non visibili allo shader</span><span class="sxs-lookup"><span data-stu-id="2f194-103">Non Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="2f194-104">Gli shader non possono fare riferimento ad alcuni heap dei descrittori tramite tabelle di descrittori, ma esistono per aiutare l'app a eseguire lo staging dei descrittori prima di registrare un elenco di comandi o perché non è necessario alcun heap visibile allo shader.</span><span class="sxs-lookup"><span data-stu-id="2f194-104">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span>

-   [<span data-ttu-id="2f194-105">Visualizzazioni non visibili</span><span class="sxs-lookup"><span data-stu-id="2f194-105">Non-visible views</span></span>](#non-visible-views)
-   [<span data-ttu-id="2f194-106">Summary</span><span class="sxs-lookup"><span data-stu-id="2f194-106">Summary</span></span>](#summary)
-   [<span data-ttu-id="2f194-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f194-107">Related topics</span></span>](#related-topics)

## <a name="non-visible-views"></a><span data-ttu-id="2f194-108">Visualizzazioni non visibili</span><span class="sxs-lookup"><span data-stu-id="2f194-108">Non-visible views</span></span>

<span data-ttu-id="2f194-109">Tutti gli heap dei descrittori, inclusi gli heap dei descrittori accessibili allo shader descritti in precedenza, possono essere manipolati dagli elenchi di CPU e/o comandi a seconda del pool di memoria e delle proprietà di accesso alla CPU selezionate dall'applicazione per un heap descrittore.</span><span class="sxs-lookup"><span data-stu-id="2f194-109">All descriptor heaps, including the shader accessible descriptor heaps described previously, can be manipulated by the CPU and/or command lists depending on the memory pool and CPU access properties the application selects for a descriptor heap.</span></span>

<span data-ttu-id="2f194-110">Per [gli heap dei descrittori](shader-visible-descriptor-heaps.md)visibili allo shader, l'ovvio motivo per negare l'accesso dello shader a questi heap dei descrittori è durante la fase di stage.</span><span class="sxs-lookup"><span data-stu-id="2f194-110">For [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md), the obvious reason to deny shader access to these descriptor heaps is while they are being staged.</span></span> <span data-ttu-id="2f194-111">Questi heap vengono quindi resi visibili allo shader e vi si accede tramite tabelle di descrittori durante l'esecuzione dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="2f194-111">Then these heaps are made shader-visible, and accessed via descriptor tables at command list execution.</span></span> <span data-ttu-id="2f194-112">Tuttavia, non è necessario eseguire lo stage degli heap visibili allo shader, che possono essere popolati direttamente.</span><span class="sxs-lookup"><span data-stu-id="2f194-112">However, there is no requirement to stage shader-visible heaps, they can be populated directly.</span></span>

<span data-ttu-id="2f194-113">Altri descrittori vengono associati alla pipeline registrando il relativo contenuto direttamente nell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="2f194-113">Other descriptors get bound to the pipeline by having their contents recorded directly into the command list.</span></span> <span data-ttu-id="2f194-114">Questi descrittori servono solo per convertire i parametri di visualizzazione al momento del record dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="2f194-114">These descriptors only serve to translate the view parameters at command list record time.</span></span> <span data-ttu-id="2f194-115">Questi heap sono sempre non visibili per lo shader e contengono quanto segue.</span><span class="sxs-lookup"><span data-stu-id="2f194-115">These heaps are always non-shader visible and contain the following.</span></span>

-   <span data-ttu-id="2f194-116">Rendering delle visualizzazioni di destinazione (RTV)</span><span class="sxs-lookup"><span data-stu-id="2f194-116">Render Target Views (RTVs)</span></span>
-   <span data-ttu-id="2f194-117">Visualizzazioni degli stencil di profondità (DSV)</span><span class="sxs-lookup"><span data-stu-id="2f194-117">Depth Stencil Views (DSVs)</span></span>

<span data-ttu-id="2f194-118">Le viste IBV (Index Buffer Views), le viste vertex buffer (VBV) e le viste di output di flusso (SOV) vengono passate direttamente ai metodi API e non hanno tipi di heap specifici.</span><span class="sxs-lookup"><span data-stu-id="2f194-118">Index Buffer Views (IBVs), Vertex Buffer Views (VBVs), and Stream Output Views (SOVs) are passed directly to API methods, are do not have specific heap types.</span></span>

<span data-ttu-id="2f194-119">Dopo la registrazione nell'elenco dei comandi ,ad esempio con una chiamata come [**OMSetRenderTargets,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)la memoria usata per contenere i descrittori per questa chiamata è immediatamente disponibile per il nuovo uso dopo la chiamata.</span><span class="sxs-lookup"><span data-stu-id="2f194-119">After recording into the command list (with a call such as [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), for example) the memory used to hold the descriptors for this call is immediately available for re-use after the call.</span></span>

<span data-ttu-id="2f194-120">Anche le tabelle descrittore hanno opzioni in cui un'app può consentire all'implementazione di scegliere di registrare il contenuto della tabella durante la registrazione dell'elenco dei comandi (anziché dereferenziare il puntatore di tabella in fase di esecuzione).</span><span class="sxs-lookup"><span data-stu-id="2f194-120">Even descriptor tables have options where an app can allow the implementation to choose to record the table contents at command list recording (rather than dereference the table pointer at execution).</span></span>

## <a name="summary"></a><span data-ttu-id="2f194-121">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="2f194-121">Summary</span></span>



|                   | <span data-ttu-id="2f194-122">Shader visibile, solo scrittura CPU</span><span class="sxs-lookup"><span data-stu-id="2f194-122">Shader visible, CPU write only</span></span>                                   | <span data-ttu-id="2f194-123">Non-shader visibile, lettura/scrittura della CPU</span><span class="sxs-lookup"><span data-stu-id="2f194-123">Non-shader visible, CPU read/write</span></span>                                       |
|-------------------|------------------------------------|----------------------------------------|
| <span data-ttu-id="2f194-124">**CBV, SRV, UAV**</span><span class="sxs-lookup"><span data-stu-id="2f194-124">**CBV, SRV, UAV**</span></span> | <span data-ttu-id="2f194-125">Sì</span><span class="sxs-lookup"><span data-stu-id="2f194-125">yes</span></span>                                | <span data-ttu-id="2f194-126">Sì</span><span class="sxs-lookup"><span data-stu-id="2f194-126">yes</span></span>                                    |
| <span data-ttu-id="2f194-127">**Campionatore**</span><span class="sxs-lookup"><span data-stu-id="2f194-127">**SAMPLER**</span></span>       | <span data-ttu-id="2f194-128">Sì</span><span class="sxs-lookup"><span data-stu-id="2f194-128">yes</span></span>                                | <span data-ttu-id="2f194-129">Sì</span><span class="sxs-lookup"><span data-stu-id="2f194-129">yes</span></span>                                    |
| <span data-ttu-id="2f194-130">**RTV**</span><span class="sxs-lookup"><span data-stu-id="2f194-130">**RTV**</span></span>           | <span data-ttu-id="2f194-131">No</span><span class="sxs-lookup"><span data-stu-id="2f194-131">no</span></span>                                 | <span data-ttu-id="2f194-132">sì</span><span class="sxs-lookup"><span data-stu-id="2f194-132">yes</span></span>                                    |
| <span data-ttu-id="2f194-133">**Dsv**</span><span class="sxs-lookup"><span data-stu-id="2f194-133">**DSV**</span></span>           | <span data-ttu-id="2f194-134">No</span><span class="sxs-lookup"><span data-stu-id="2f194-134">no</span></span>                                 | <span data-ttu-id="2f194-135">sì</span><span class="sxs-lookup"><span data-stu-id="2f194-135">yes</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="2f194-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f194-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f194-137">Heap dei descrittori</span><span class="sxs-lookup"><span data-stu-id="2f194-137">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




