---
title: Heap descrittori non shader visibili
description: Per gli shader non è possibile fare riferimento ad alcuni heap del descrittore tramite le tabelle dei descrittori, ma esistono per supportare l'app nella gestione temporanea dei descrittori prima di registrare un elenco di comandi o perché non è necessario alcun heap visibile dello shader.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894640cde142f1241b088518ba7140ffb9405152
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548809"
---
# <a name="non-shader-visible-descriptor-heaps"></a><span data-ttu-id="0367d-103">Heap descrittori non shader visibili</span><span class="sxs-lookup"><span data-stu-id="0367d-103">Non Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="0367d-104">Per gli shader non è possibile fare riferimento ad alcuni heap del descrittore tramite le tabelle dei descrittori, ma esistono per supportare l'app nella gestione temporanea dei descrittori prima di registrare un elenco di comandi o perché non è necessario alcun heap visibile dello shader.</span><span class="sxs-lookup"><span data-stu-id="0367d-104">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span>

-   [<span data-ttu-id="0367d-105">Viste non visibili</span><span class="sxs-lookup"><span data-stu-id="0367d-105">Non-visible views</span></span>](#non-visible-views)
-   [<span data-ttu-id="0367d-106">Summary</span><span class="sxs-lookup"><span data-stu-id="0367d-106">Summary</span></span>](#summary)
-   [<span data-ttu-id="0367d-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0367d-107">Related topics</span></span>](#related-topics)

## <a name="non-visible-views"></a><span data-ttu-id="0367d-108">Viste non visibili</span><span class="sxs-lookup"><span data-stu-id="0367d-108">Non-visible views</span></span>

<span data-ttu-id="0367d-109">Tutti gli heap dei descrittori, inclusi gli heap dei descrittori accessibili dello shader descritti in precedenza, possono essere modificati dagli elenchi della CPU e/o dei comandi a seconda del pool di memoria e delle proprietà di accesso alla CPU che l'applicazione seleziona per un heap del descrittore.</span><span class="sxs-lookup"><span data-stu-id="0367d-109">All descriptor heaps, including the shader accessible descriptor heaps described previously, can be manipulated by the CPU and/or command lists depending on the memory pool and CPU access properties the application selects for a descriptor heap.</span></span>

<span data-ttu-id="0367d-110">Per gli [heap del descrittore visibile dello shader](shader-visible-descriptor-heaps.md), il motivo più ovvio per negare l'accesso dello shader a questi heap di descrittori è mentre sono in fase di gestione temporanea.</span><span class="sxs-lookup"><span data-stu-id="0367d-110">For [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md), the obvious reason to deny shader access to these descriptor heaps is while they are being staged.</span></span> <span data-ttu-id="0367d-111">Questi heap, quindi, vengono resi visibili allo shader e sono accessibili tramite tabelle descrittore nell'esecuzione dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="0367d-111">Then these heaps are made shader-visible, and accessed via descriptor tables at command list execution.</span></span> <span data-ttu-id="0367d-112">Tuttavia, non esiste alcun requisito per gestire gli heap visibili dello shader, che possono essere popolati direttamente.</span><span class="sxs-lookup"><span data-stu-id="0367d-112">However, there is no requirement to stage shader-visible heaps, they can be populated directly.</span></span>

<span data-ttu-id="0367d-113">Gli altri descrittori vengono associati alla pipeline con il relativo contenuto registrato direttamente nell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="0367d-113">Other descriptors get bound to the pipeline by having their contents recorded directly into the command list.</span></span> <span data-ttu-id="0367d-114">Questi descrittori servono solo per tradurre i parametri di visualizzazione in fase di record dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="0367d-114">These descriptors only serve to translate the view parameters at command list record time.</span></span> <span data-ttu-id="0367d-115">Questi heap sono sempre visibili senza shader e contengono quanto segue.</span><span class="sxs-lookup"><span data-stu-id="0367d-115">These heaps are always non-shader visible and contain the following.</span></span>

-   <span data-ttu-id="0367d-116">Visualizzazioni destinazione rendering (RTVs)</span><span class="sxs-lookup"><span data-stu-id="0367d-116">Render Target Views (RTVs)</span></span>
-   <span data-ttu-id="0367d-117">Visualizzazioni stencil Depth (viste origine dati)</span><span class="sxs-lookup"><span data-stu-id="0367d-117">Depth Stencil Views (DSVs)</span></span>

<span data-ttu-id="0367d-118">Le viste del buffer di indice (IBVs), le viste del buffer dei vertici (VBVs) e le viste di output del flusso (sovietici) vengono passate direttamente ai metodi API, non dispongono di tipi di heap specifici.</span><span class="sxs-lookup"><span data-stu-id="0367d-118">Index Buffer Views (IBVs), Vertex Buffer Views (VBVs), and Stream Output Views (SOVs) are passed directly to API methods, are do not have specific heap types.</span></span>

<span data-ttu-id="0367d-119">Dopo la registrazione nell'elenco dei comandi (ad esempio, con una chiamata come [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)), la memoria usata per conservare i descrittori per questa chiamata è immediatamente disponibile per essere riutilizzata dopo la chiamata.</span><span class="sxs-lookup"><span data-stu-id="0367d-119">After recording into the command list (with a call such as [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), for example) the memory used to hold the descriptors for this call is immediately available for re-use after the call.</span></span>

<span data-ttu-id="0367d-120">Anche le tabelle dei descrittori includono opzioni in cui un'app può consentire all'implementazione di scegliere di registrare il contenuto della tabella nella registrazione dell'elenco di comandi, anziché dereferenziare il puntatore della tabella in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0367d-120">Even descriptor tables have options where an app can allow the implementation to choose to record the table contents at command list recording (rather than dereference the table pointer at execution).</span></span>

## <a name="summary"></a><span data-ttu-id="0367d-121">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="0367d-121">Summary</span></span>



|                   |                                    |                                        |
|-------------------|------------------------------------|----------------------------------------|
|                   | <span data-ttu-id="0367d-122">**shader visibile, solo scrittura CPU**</span><span class="sxs-lookup"><span data-stu-id="0367d-122">**shader visible, CPU write only**</span></span> | <span data-ttu-id="0367d-123">**non shader visibile, lettura/scrittura CPU**</span><span class="sxs-lookup"><span data-stu-id="0367d-123">**non-shader visible, CPU read/write**</span></span> |
| <span data-ttu-id="0367d-124">**CBV, SRV, UAV**</span><span class="sxs-lookup"><span data-stu-id="0367d-124">**CBV, SRV, UAV**</span></span> | <span data-ttu-id="0367d-125">sì</span><span class="sxs-lookup"><span data-stu-id="0367d-125">yes</span></span>                                | <span data-ttu-id="0367d-126">sì</span><span class="sxs-lookup"><span data-stu-id="0367d-126">yes</span></span>                                    |
| <span data-ttu-id="0367d-127">**CAMPIONATORE**</span><span class="sxs-lookup"><span data-stu-id="0367d-127">**SAMPLER**</span></span>       | <span data-ttu-id="0367d-128">sì</span><span class="sxs-lookup"><span data-stu-id="0367d-128">yes</span></span>                                | <span data-ttu-id="0367d-129">sì</span><span class="sxs-lookup"><span data-stu-id="0367d-129">yes</span></span>                                    |
| <span data-ttu-id="0367d-130">**RTV**</span><span class="sxs-lookup"><span data-stu-id="0367d-130">**RTV**</span></span>           | <span data-ttu-id="0367d-131">no</span><span class="sxs-lookup"><span data-stu-id="0367d-131">no</span></span>                                 | <span data-ttu-id="0367d-132">sì</span><span class="sxs-lookup"><span data-stu-id="0367d-132">yes</span></span>                                    |
| <span data-ttu-id="0367d-133">**DSV**</span><span class="sxs-lookup"><span data-stu-id="0367d-133">**DSV**</span></span>           | <span data-ttu-id="0367d-134">no</span><span class="sxs-lookup"><span data-stu-id="0367d-134">no</span></span>                                 | <span data-ttu-id="0367d-135">sì</span><span class="sxs-lookup"><span data-stu-id="0367d-135">yes</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="0367d-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0367d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0367d-137">Heap descrittore</span><span class="sxs-lookup"><span data-stu-id="0367d-137">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




