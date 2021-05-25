---
title: Uso delle barriere delle risorse per sincronizzare gli stati delle risorse in Direct3D 12
description: Per ridurre l'utilizzo complessivo della CPU e abilitare il multithreading dei driver e la pre-elaborazione, Direct3D 12 sposta la responsabilità della gestione dello stato per risorsa dal driver di grafica all'applicazione.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df27e7997b4f3f56ae8e87688e5cc136dc7eb87d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343476"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a><span data-ttu-id="a69a6-103">Uso delle barriere delle risorse per sincronizzare gli stati delle risorse in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a69a6-103">Using Resource Barriers to Synchronize Resource States in Direct3D 12</span></span>

<span data-ttu-id="a69a6-104">Per ridurre l'utilizzo complessivo della CPU e abilitare il multithreading dei driver e la pre-elaborazione, Direct3D 12 sposta la responsabilità della gestione dello stato per risorsa dal driver di grafica all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a69a6-104">To reduce overall CPU usage and enable driver multi-threading and pre-processing, Direct3D 12 moves the responsibility of per-resource state management from the graphics driver to the application.</span></span> <span data-ttu-id="a69a6-105">Un esempio di stato per risorsa è se è attualmente in corso l'accesso a una risorsa trama come tramite un Shader Resource View o come visualizzazione di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="a69a6-105">An example of per-resource state is whether a texture resource is currently being accessed as through a Shader Resource View or as a Render Target View.</span></span> <span data-ttu-id="a69a6-106">In Direct3D 11 i driver dovevano tenere traccia di questo stato in background.</span><span class="sxs-lookup"><span data-stu-id="a69a6-106">In Direct3D 11, drivers were required to track this state in the background.</span></span> <span data-ttu-id="a69a6-107">Questa operazione è costosa dal punto di vista della CPU e complica significativamente qualsiasi tipo di progettazione multi-thread.</span><span class="sxs-lookup"><span data-stu-id="a69a6-107">This is expensive from a CPU perspective and significantly complicates any sort of multi-threaded design.</span></span> <span data-ttu-id="a69a6-108">In Microsoft Direct3D 12 la maggior parte dello stato per risorsa viene gestita dall'applicazione con una singola API, [**ID3D12GraphicsCommandList::ResourceBarrier.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)</span><span class="sxs-lookup"><span data-stu-id="a69a6-108">In Microsoft Direct3D 12, most per-resource state is managed by the application with a single API, [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>

-   [<span data-ttu-id="a69a6-109">Uso dell'API ResourceBarrier per gestire lo stato per ogni risorsa</span><span class="sxs-lookup"><span data-stu-id="a69a6-109">Using the ResourceBarrier API to manage per-resource state</span></span>](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [<span data-ttu-id="a69a6-110">Stati delle risorse</span><span class="sxs-lookup"><span data-stu-id="a69a6-110">Resource states</span></span>](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [<span data-ttu-id="a69a6-111">Stati iniziali per le risorse</span><span class="sxs-lookup"><span data-stu-id="a69a6-111">Initial states for resources</span></span>](#initial-states-for-resources)
    -   [<span data-ttu-id="a69a6-112">Restrizioni dello stato delle risorse di lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a69a6-112">Read/write resource state restrictions</span></span>](#readwrite-resource-state-restrictions)
    -   [<span data-ttu-id="a69a6-113">Stati delle risorse per la presentazione dei buffer nascosto</span><span class="sxs-lookup"><span data-stu-id="a69a6-113">Resource states for presenting back buffers</span></span>](#resource-states-for-presenting-back-buffers)
    -   [<span data-ttu-id="a69a6-114">Rimozione delle risorse</span><span class="sxs-lookup"><span data-stu-id="a69a6-114">Discarding resources</span></span>](#discarding-resources)
-   [<span data-ttu-id="a69a6-115">Transizioni di stato implicite</span><span class="sxs-lookup"><span data-stu-id="a69a6-115">Implicit State Transitions</span></span>](#implicit-state-transitions)
    -   [<span data-ttu-id="a69a6-116">Promozione dello stato comune</span><span class="sxs-lookup"><span data-stu-id="a69a6-116">Common state promotion</span></span>](#common-state-promotion)
    -   [<span data-ttu-id="a69a6-117">Decadimento dello stato a comune</span><span class="sxs-lookup"><span data-stu-id="a69a6-117">State decay to common</span></span>](#state-decay-to-common)
    -   [<span data-ttu-id="a69a6-118">Implicazioni per le prestazioni</span><span class="sxs-lookup"><span data-stu-id="a69a6-118">Performance implications</span></span>](#performance-implications)
-   [<span data-ttu-id="a69a6-119">Split Barriers</span><span class="sxs-lookup"><span data-stu-id="a69a6-119">Split Barriers</span></span>](#split-barriers)
-   [<span data-ttu-id="a69a6-120">Scenario di esempio di barriera delle risorse</span><span class="sxs-lookup"><span data-stu-id="a69a6-120">Resource barrier example scenario</span></span>](#resource-barrier-example-scenario)
-   [<span data-ttu-id="a69a6-121">Esempio comune di promozione e decadimento dello stato</span><span class="sxs-lookup"><span data-stu-id="a69a6-121">Common state promotion and decay sample</span></span>](#common-state-promotion-and-decay-sample)
-   [<span data-ttu-id="a69a6-122">Esempio di barriere di divisione</span><span class="sxs-lookup"><span data-stu-id="a69a6-122">Example of split barriers</span></span>](#example-of-split-barriers)
-   [<span data-ttu-id="a69a6-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a69a6-123">Related topics</span></span>](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a><span data-ttu-id="a69a6-124">Uso dell'API ResourceBarrier per gestire lo stato per ogni risorsa</span><span class="sxs-lookup"><span data-stu-id="a69a6-124">Using the ResourceBarrier API to manage per-resource state</span></span>

<span data-ttu-id="a69a6-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifica al driver di grafica le situazioni in cui il driver potrebbe dover sincronizzare più accessi alla memoria in cui è archiviata una risorsa.</span><span class="sxs-lookup"><span data-stu-id="a69a6-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifies the graphics driver of situations in which the driver may need to synchronize multiple accesses to the memory in which a resource is stored.</span></span> <span data-ttu-id="a69a6-126">Il metodo viene chiamato con una o più strutture di descrizione della barriera delle risorse che indicano il tipo di barriera di risorse dichiarato.</span><span class="sxs-lookup"><span data-stu-id="a69a6-126">The method is called with one or more resource barrier description structures indicating the type of resource barrier being declared.</span></span>

<span data-ttu-id="a69a6-127">Esistono tre tipi di barriere alle risorse:</span><span class="sxs-lookup"><span data-stu-id="a69a6-127">There are three types of resource barriers:</span></span>

-   <span data-ttu-id="a69a6-128">**Barriera di transizione:** una barriera di transizione indica che un set di sottorisorse esegue la transizione tra utilizzi diversi.</span><span class="sxs-lookup"><span data-stu-id="a69a6-128">**Transition barrier** - A transition barrier indicates that a set of subresources transition between different usages.</span></span> <span data-ttu-id="a69a6-129">Una [**struttura D3D12 \_ RESOURCE TRANSITION \_ \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) viene usata per specificare la sottorisorsa in fase di transizione, nonché gli stati *prima* e dopo della sottorisorsa. </span><span class="sxs-lookup"><span data-stu-id="a69a6-129">A [**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) structure is used to specify the subresource that is transitioning as well as the *before* and *after* states of the subresource.</span></span>

    <span data-ttu-id="a69a6-130">Il sistema verifica che le transizioni di sottorisorse in un elenco di comandi siano coerenti con le transizioni precedenti nello stesso elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="a69a6-130">The system verifies that subresource transitions in a command list are consistent with previous transitions in the same command list.</span></span> <span data-ttu-id="a69a6-131">Il livello di debug tiene inoltre traccia dello stato della sottorisorsa per trovare altri errori, ma questa convalida è conservativa e non esaustiva.</span><span class="sxs-lookup"><span data-stu-id="a69a6-131">The debug layer further tracks subresource state to find other errors however this validation is conservative and not exhaustive.</span></span>

    <span data-ttu-id="a69a6-132">Si noti che è possibile usare il flag D3D12 RESOURCE BARRIER ALL SUBRESOURCES per specificare che è in corso la transizione di tutte le \_ \_ \_ \_ sottorisorse all'interno di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="a69a6-132">Note that you can use the D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES flag to specify that all subresources within a resource are being transitioned.</span></span>

-   <span data-ttu-id="a69a6-133">**Barriera di aliasing:** una barriera di aliasing indica una transizione tra gli utilizzi di due risorse diverse che hanno mapping sovrapposti nello stesso heap.</span><span class="sxs-lookup"><span data-stu-id="a69a6-133">**Aliasing barrier** - An aliasing barrier indicates a transition between usages of two different resources which have overlapping mappings into the same heap.</span></span> <span data-ttu-id="a69a6-134">Questo vale sia per le risorse riservate che per le risorse inserite.</span><span class="sxs-lookup"><span data-stu-id="a69a6-134">This applies to both reserved and placed resources.</span></span> <span data-ttu-id="a69a6-135">Una [**struttura D3D12 \_ RESOURCE \_ ALIASING \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) viene usata per specificare sia la risorsa *prima* che la *risorsa dopo.*</span><span class="sxs-lookup"><span data-stu-id="a69a6-135">A [**D3D12\_RESOURCE\_ALIASING\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) structure is used to specify both the *before* resource and the *after* resource.</span></span>

    <span data-ttu-id="a69a6-136">Si noti che una o entrambe le risorse possono essere NULL, a indicare che qualsiasi risorsa affiancata potrebbe causare l'aliasing.</span><span class="sxs-lookup"><span data-stu-id="a69a6-136">Note that one or both resources can be NULL, which indicates that any tiled resource could cause aliasing.</span></span> <span data-ttu-id="a69a6-137">Per altre informazioni sull'uso delle risorse affiancate, vedere [Risorse affiancate](../direct3d11/tiled-resources.md) e [Risorse in riquadri del volume](volume-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="a69a6-137">For more information about using tiled resources, see [Tiled resources](../direct3d11/tiled-resources.md) and [Volume Tiled Resources](volume-tiled-resources.md).</span></span>

-   <span data-ttu-id="a69a6-138">Barriera della visualizzazione di accesso non ordinato : una barriera di **UAV** indica che tutti gli accessi UAV, sia in lettura che in scrittura, a una determinata risorsa devono essere completati tra gli accessi UAV futuri, sia in lettura che in scrittura.</span><span class="sxs-lookup"><span data-stu-id="a69a6-138">**Unordered access view (UAV) barrier** - A UAV barrier indicates that all UAV accesses, both read or write, to a particular resource must complete between any future UAV accesses, both read or write.</span></span> <span data-ttu-id="a69a6-139">Non è necessario che un'app metta una barriera UAV tra due chiamate di disegno o invio che leggono solo da un UAV.</span><span class="sxs-lookup"><span data-stu-id="a69a6-139">It's not necessary for an app to put a UAV barrier between two draw or dispatch calls that only read from a UAV.</span></span> <span data-ttu-id="a69a6-140">Inoltre, non è necessario inserire una barriera UAV tra due chiamate di disegno o invio che scrivono nello stesso UAV se l'applicazione sa che è sicuro eseguire l'accesso UAV in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="a69a6-140">Also, it's not necessary to put a UAV barrier between two draw or dispatch calls that write to the same UAV if the application knows that it is safe to execute the UAV access in any order.</span></span> <span data-ttu-id="a69a6-141">Una [**struttura D3D12 \_ RESOURCE \_ UAV \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) viene usata per specificare la risorsa UAV a cui si applica la barriera.</span><span class="sxs-lookup"><span data-stu-id="a69a6-141">A [**D3D12\_RESOURCE\_UAV\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) structure is used to specify the UAV resource to which the barrier applies.</span></span> <span data-ttu-id="a69a6-142">L'applicazione può specificare NULL per l'UAV della barriera, che indica che qualsiasi accesso UAV potrebbe richiedere la barriera.</span><span class="sxs-lookup"><span data-stu-id="a69a6-142">The application can specify NULL for the barrier's UAV, which indicates that any UAV access could require the barrier.</span></span>

<span data-ttu-id="a69a6-143">Quando [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) viene chiamato con una matrice di descrizioni della barriera di risorse, l'API si comporta come se fosse stata chiamata una volta per ogni elemento, nell'ordine in cui sono stati forniti.</span><span class="sxs-lookup"><span data-stu-id="a69a6-143">When [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) is called with an array of resource barrier descriptions, the API behaves as if it was called once for each element, in the order in which they were supplied.</span></span>

<span data-ttu-id="a69a6-144">In qualsiasi momento, una sottorisorsa si trova esattamente in uno stato, determinato dal set di flag [**D3D12 \_ RESOURCE \_ STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) forniti a [**ResourceBarrier.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)</span><span class="sxs-lookup"><span data-stu-id="a69a6-144">At any given time, a subresource is in exactly one state, determined by the set of [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) flags supplied to [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span> <span data-ttu-id="a69a6-145">L'applicazione deve garantire che gli *stati prima* e *dopo* le chiamate consecutive a **ResourceBarrier siano d'accordo.**</span><span class="sxs-lookup"><span data-stu-id="a69a6-145">The application must ensure that the *before* and *after* states of consecutive calls to **ResourceBarrier** agree.</span></span>

> [!TIP]
>
> <span data-ttu-id="a69a6-146">Le applicazioni devono eseguire più transizioni in batch in un'unica chiamata API, laddove possibile.</span><span class="sxs-lookup"><span data-stu-id="a69a6-146">Applications should batch multiple transitions into one API call wherever possible.</span></span>

 

### <a name="resource-states"></a><span data-ttu-id="a69a6-147">Stati delle risorse</span><span class="sxs-lookup"><span data-stu-id="a69a6-147">Resource states</span></span>

<span data-ttu-id="a69a6-148">Per l'elenco completo degli stati delle risorse tra cui una risorsa può eseguire la transizione, vedere l'argomento di riferimento per [**l'enumerazione D3D12 \_ RESOURCE \_ STATES.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="a69a6-148">For the complete list of resource states that a resource can transition between, see the reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) enumeration.</span></span>

<span data-ttu-id="a69a6-149">Per le barriere di suddivisione delle risorse, vedere [**anche D3D12 \_ RESOURCE BARRIER \_ \_ FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span><span class="sxs-lookup"><span data-stu-id="a69a6-149">For split resource barriers, also refer to [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span></span>

### <a name="initial-states-for-resources"></a><span data-ttu-id="a69a6-150">Stati iniziali per le risorse</span><span class="sxs-lookup"><span data-stu-id="a69a6-150">Initial states for resources</span></span>

<span data-ttu-id="a69a6-151">Le risorse possono essere create con qualsiasi stato iniziale specificato dall'utente (valido per la descrizione della risorsa), con le eccezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a69a6-151">Resources may be created with any user-specified initial state (valid for the resource description), with the following exceptions:</span></span>

-   <span data-ttu-id="a69a6-152">Gli heap di caricamento devono iniziare con lo stato D3D12 RESOURCE STATE GENERIC READ, che è una combinazione \_ OR bit per bit \_ \_ \_ di:</span><span class="sxs-lookup"><span data-stu-id="a69a6-152">Upload heaps must start out in the state D3D12\_RESOURCE\_STATE\_GENERIC\_READ which is a bitwise OR combination of:</span></span>
    -   <span data-ttu-id="a69a6-153">VERTICE DELLO STATO DELLA RISORSA D3D12 \_ \_ E BUFFER \_ \_ \_ \_ COSTANTE</span><span class="sxs-lookup"><span data-stu-id="a69a6-153">D3D12\_RESOURCE\_STATE\_VERTEX\_AND\_CONSTANT\_BUFFER</span></span>
    -   <span data-ttu-id="a69a6-154">BUFFER DELL'INDICE DELLO \_ \_ STATO DELLA \_ RISORSA \_ D3D12</span><span class="sxs-lookup"><span data-stu-id="a69a6-154">D3D12\_RESOURCE\_STATE\_INDEX\_BUFFER</span></span>
    -   <span data-ttu-id="a69a6-155">ORIGINE COPIA STATO RISORSA D3D12 \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a69a6-155">D3D12\_RESOURCE\_STATE\_COPY\_SOURCE</span></span>
    -   <span data-ttu-id="a69a6-156">RISORSA D3D12 \_ RESOURCE STATE NON PIXEL \_ \_ \_ \_ \_ SHADER</span><span class="sxs-lookup"><span data-stu-id="a69a6-156">D3D12\_RESOURCE\_STATE\_NON\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="a69a6-157">RISORSA \_ \_ PIXEL \_ \_ SHADER \_ DELLO STATO DELLA RISORSA D3D12</span><span class="sxs-lookup"><span data-stu-id="a69a6-157">D3D12\_RESOURCE\_STATE\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="a69a6-158">ARGOMENTO INDIRETTO DELLO STATO DELLA RISORSA D3D12 \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a69a6-158">D3D12\_RESOURCE\_STATE\_INDIRECT\_ARGUMENT</span></span>
-   <span data-ttu-id="a69a6-159">Gli heap di readback devono essere avviati nello stato D3D12 \_ RESOURCE \_ STATE COPY \_ \_ DEST.</span><span class="sxs-lookup"><span data-stu-id="a69a6-159">Readback heaps must start out in the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span>
-   <span data-ttu-id="a69a6-160">I buffer back della catena di scambio vengono avviati automaticamente nello stato D3D12 \_ RESOURCE \_ STATE \_ COMMON.</span><span class="sxs-lookup"><span data-stu-id="a69a6-160">Swap chain back buffers automatically start out in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span>

<span data-ttu-id="a69a6-161">Prima che un heap possa essere la destinazione di un'operazione di copia GPU, in genere l'heap deve essere passato allo stato D3D12 \_ RESOURCE \_ STATE COPY \_ \_ DEST.</span><span class="sxs-lookup"><span data-stu-id="a69a6-161">Before a heap can be the target of a GPU copy operation, normally the heap must first be transitioned to the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span> <span data-ttu-id="a69a6-162">Tuttavia, le risorse create negli heap UPLOAD devono iniziare in e non possono passare dallo stato GENERIC READ perché solo la CPU sta \_ eseguendo la scrittura.</span><span class="sxs-lookup"><span data-stu-id="a69a6-162">However, resources created on UPLOAD heaps must start in and cannot change from the GENERIC\_READ state since only the CPU will be doing writing.</span></span> <span data-ttu-id="a69a6-163">Al contrario, le risorse di cui è stato eseguito il commit create negli heap READBACK devono iniziare in e non possono cambiare dallo stato COPY \_ DEST.</span><span class="sxs-lookup"><span data-stu-id="a69a6-163">Conversely, committed resources created in READBACK heaps must start in and cannot change from the COPY\_DEST state.</span></span>

### <a name="readwrite-resource-state-restrictions"></a><span data-ttu-id="a69a6-164">Restrizioni relative allo stato delle risorse di lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a69a6-164">Read/write resource state restrictions</span></span>

<span data-ttu-id="a69a6-165">I bit di utilizzo dello stato della risorsa usati per descrivere uno stato della risorsa sono suddivisi in stati di sola lettura e di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a69a6-165">The resource state usage bits that are used to describe a resource state are divided into read-only and read/write states.</span></span> <span data-ttu-id="a69a6-166">L'argomento di riferimento [**per D3D12 \_ RESOURCE \_ STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indica il livello di accesso in lettura/scrittura per ogni bit nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="a69a6-166">The reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indicates the read/write access level for each bit in the enumeration.</span></span>

<span data-ttu-id="a69a6-167">Al massimo, è possibile impostare un solo bit di lettura/scrittura per qualsiasi risorsa.</span><span class="sxs-lookup"><span data-stu-id="a69a6-167">At most, only one read/write bit can be set for any resource.</span></span> <span data-ttu-id="a69a6-168">Se è impostato un bit di scrittura, non è possibile impostare alcun bit di sola lettura per tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="a69a6-168">If a write bit is set, then no read-only bit may be set for that resource.</span></span> <span data-ttu-id="a69a6-169">Se non è impostato alcun bit di scrittura, è possibile impostare un numero qualsiasi di bit di lettura.</span><span class="sxs-lookup"><span data-stu-id="a69a6-169">If no write bit is set, then any number of read bits may be set.</span></span>

### <a name="resource-states-for-presenting-back-buffers"></a><span data-ttu-id="a69a6-170">Stati delle risorse per la presentazione di buffer back</span><span class="sxs-lookup"><span data-stu-id="a69a6-170">Resource states for presenting back buffers</span></span>

<span data-ttu-id="a69a6-171">Prima di presentare un buffer nascosto, deve essere nello stato D3D12 \_ RESOURCE \_ STATE \_ COMMON.</span><span class="sxs-lookup"><span data-stu-id="a69a6-171">Before a back buffer is presented, it must be in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span> <span data-ttu-id="a69a6-172">Si noti che lo stato della risorsa D3D12 RESOURCE STATE PRESENT è un sinonimo di \_ \_ \_ D3D12 RESOURCE STATE COMMON ed entrambi hanno un valore \_ \_ pari a \_ 0.</span><span class="sxs-lookup"><span data-stu-id="a69a6-172">Note, the resource state D3D12\_RESOURCE\_STATE\_PRESENT is a synonym for D3D12\_RESOURCE\_STATE\_COMMON, and they both have a value of 0.</span></span> <span data-ttu-id="a69a6-173">Se [**IDXGISwapChain::P resent**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (o [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) viene chiamato su una risorsa che non è attualmente in questo stato, viene generato un avviso del livello di debug.</span><span class="sxs-lookup"><span data-stu-id="a69a6-173">If [**IDXGISwapChain::Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (or [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) is called on a resource that is not currently in this state, a debug layer warning is emitted.</span></span>

### <a name="discarding-resources"></a><span data-ttu-id="a69a6-174">Rimozione delle risorse</span><span class="sxs-lookup"><span data-stu-id="a69a6-174">Discarding resources</span></span>

<span data-ttu-id="a69a6-175">Tutte le sottorisorse in una risorsa devono essere nello stato RENDER TARGET o DEPTH WRITE, rispettivamente per le destinazioni di rendering/le risorse depth-stencil, quando viene chiamato \_ \_ [**ID3D12GraphicsCommandList::D iscardResource.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)</span><span class="sxs-lookup"><span data-stu-id="a69a6-175">All subresources in a resource must be in the RENDER\_TARGET state, or DEPTH\_WRITE state, for render targets/depth-stencil resources respectively, when [**ID3D12GraphicsCommandList::DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) is called.</span></span>

## <a name="implicit-state-transitions"></a><span data-ttu-id="a69a6-176">Transizioni di stato implicite</span><span class="sxs-lookup"><span data-stu-id="a69a6-176">Implicit State Transitions</span></span>

<span data-ttu-id="a69a6-177">Le risorse possono essere "promosse" solo al di fuori di D3D12 \_ RESOURCE \_ STATE \_ COMMON.</span><span class="sxs-lookup"><span data-stu-id="a69a6-177">Resources can only be "promoted" out of D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="a69a6-178">Analogamente, le risorse "decadono" solo a D3D12 \_ RESOURCE \_ STATE \_ COMMON.</span><span class="sxs-lookup"><span data-stu-id="a69a6-178">Similarly, resources will only "decay" to D3D12\_RESOURCE\_STATE\_COMMON.</span></span>

### <a name="common-state-promotion"></a><span data-ttu-id="a69a6-179">Promozione dello stato comune</span><span class="sxs-lookup"><span data-stu-id="a69a6-179">Common state promotion</span></span>

<span data-ttu-id="a69a6-180">Tutte le risorse del buffer e le trame con il flag DI RISORSA D3D12 ALLOW SIMULTANEOUS ACCESS impostato vengono \_ \_ promosse implicitamente da \_ \_ \_ D3D12 RESOURCE STATE \_ COMMON \_ \_ \_ allo stato pertinente al primo accesso alla GPU, inclusa la lettura generica per coprire qualsiasi scenario di lettura.</span><span class="sxs-lookup"><span data-stu-id="a69a6-180">All buffer resources as well as textures with the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set are implicitly promoted from D3D12\_RESOURCE\_STATE\_COMMON to the relevant state on first GPU access, including GENERIC\_READ to cover any read scenario.</span></span> <span data-ttu-id="a69a6-181">È possibile accedere a qualsiasi risorsa nello stato COMMON come se si trovava in un unico stato con</span><span class="sxs-lookup"><span data-stu-id="a69a6-181">Any resource in the COMMON state can be accessed as through it were in a single state with</span></span>

<dl> <span data-ttu-id="a69a6-182">1 flag WRITE o</span><span class="sxs-lookup"><span data-stu-id="a69a6-182">1 WRITE flag, or</span></span>  
<span data-ttu-id="a69a6-183">1 o più flag READ</span><span class="sxs-lookup"><span data-stu-id="a69a6-183">1 or more READ flags</span></span>  
</dl>

<span data-ttu-id="a69a6-184">Le risorse possono essere promosse dallo stato COMMON in base alla tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="a69a6-184">Resources can be promoted from the COMMON state based on the following table:</span></span>



| <span data-ttu-id="a69a6-185">Flag di stato</span><span class="sxs-lookup"><span data-stu-id="a69a6-185">State flag</span></span>                    | <span data-ttu-id="a69a6-186">Buffer e Simultaneous-Access trame</span><span class="sxs-lookup"><span data-stu-id="a69a6-186">Buffers and Simultaneous-Access Textures</span></span>                             | <span data-ttu-id="a69a6-187">Trame ad accesso non simultaneo</span><span class="sxs-lookup"><span data-stu-id="a69a6-187">Non-Simultaneous-Access Textures</span></span>                                     |
|-------------------------------|----------------------------------------------|--------------------------------------|
| <span data-ttu-id="a69a6-188">VERTEX \_ E \_ CONSTANT \_ BUFFER</span><span class="sxs-lookup"><span data-stu-id="a69a6-188">VERTEX\_AND\_CONSTANT\_BUFFER</span></span> | <span data-ttu-id="a69a6-189">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-189">Yes</span></span>                                          | <span data-ttu-id="a69a6-190">No</span><span class="sxs-lookup"><span data-stu-id="a69a6-190">No</span></span>                                   |
| <span data-ttu-id="a69a6-191">INDEX \_ BUFFER</span><span class="sxs-lookup"><span data-stu-id="a69a6-191">INDEX\_BUFFER</span></span>                 | <span data-ttu-id="a69a6-192">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-192">Yes</span></span>                                          | <span data-ttu-id="a69a6-193">No</span><span class="sxs-lookup"><span data-stu-id="a69a6-193">No</span></span>                                   |
| <span data-ttu-id="a69a6-194">DESTINAZIONE DI \_ RENDERING</span><span class="sxs-lookup"><span data-stu-id="a69a6-194">RENDER\_TARGET</span></span>                | <span data-ttu-id="a69a6-195">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-195">Yes</span></span>                                          | <span data-ttu-id="a69a6-196">No</span><span class="sxs-lookup"><span data-stu-id="a69a6-196">No</span></span>                                   |
| <span data-ttu-id="a69a6-197">ACCESSO NON \_ ORDINATO</span><span class="sxs-lookup"><span data-stu-id="a69a6-197">UNORDERED\_ACCESS</span></span>             | <span data-ttu-id="a69a6-198">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-198">Yes</span></span>                                          | <span data-ttu-id="a69a6-199">No</span><span class="sxs-lookup"><span data-stu-id="a69a6-199">No</span></span>                                   |
| <span data-ttu-id="a69a6-200">SCRITTURA \_ PROFONDITÀ</span><span class="sxs-lookup"><span data-stu-id="a69a6-200">DEPTH\_WRITE</span></span>                  | <span data-ttu-id="a69a6-201">No<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a69a6-201">No<sup>\*</sup></span></span>                              | <span data-ttu-id="a69a6-202">No</span><span class="sxs-lookup"><span data-stu-id="a69a6-202">No</span></span>                                   |
| <span data-ttu-id="a69a6-203">LETTURA \_ DI PROFONDITÀ</span><span class="sxs-lookup"><span data-stu-id="a69a6-203">DEPTH\_READ</span></span>                   | <span data-ttu-id="a69a6-204">No<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a69a6-204">No<sup>\*</sup></span></span>                              | <span data-ttu-id="a69a6-205">No</span><span class="sxs-lookup"><span data-stu-id="a69a6-205">No</span></span>                                   |
| <span data-ttu-id="a69a6-206">RISORSA NON \_ PIXEL \_ \_ SHADER</span><span class="sxs-lookup"><span data-stu-id="a69a6-206">NON\_PIXEL\_SHADER\_RESOURCE</span></span>  | <span data-ttu-id="a69a6-207">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-207">Yes</span></span>                                          | <span data-ttu-id="a69a6-208">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-208">Yes</span></span>                                  |
| <span data-ttu-id="a69a6-209">RISORSA PIXEL \_ \_ SHADER</span><span class="sxs-lookup"><span data-stu-id="a69a6-209">PIXEL\_SHADER\_RESOURCE</span></span>       | <span data-ttu-id="a69a6-210">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-210">Yes</span></span>                                          | <span data-ttu-id="a69a6-211">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-211">Yes</span></span>                                  |
| <span data-ttu-id="a69a6-212">STREAM \_ OUT</span><span class="sxs-lookup"><span data-stu-id="a69a6-212">STREAM\_OUT</span></span>                   | <span data-ttu-id="a69a6-213">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-213">Yes</span></span>                                          | <span data-ttu-id="a69a6-214">No</span><span class="sxs-lookup"><span data-stu-id="a69a6-214">No</span></span>                                   |
| <span data-ttu-id="a69a6-215">ARGOMENTO \_ INDIRETTO</span><span class="sxs-lookup"><span data-stu-id="a69a6-215">INDIRECT\_ARGUMENT</span></span>            | <span data-ttu-id="a69a6-216">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-216">Yes</span></span>                                          | <span data-ttu-id="a69a6-217">No</span><span class="sxs-lookup"><span data-stu-id="a69a6-217">No</span></span>                                   |
| <span data-ttu-id="a69a6-218">COPIA \_ DEST</span><span class="sxs-lookup"><span data-stu-id="a69a6-218">COPY\_DEST</span></span>                    | <span data-ttu-id="a69a6-219">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-219">Yes</span></span>                                          | <span data-ttu-id="a69a6-220">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-220">Yes</span></span>                                  |
| <span data-ttu-id="a69a6-221">COPIA \_ ORIGINE</span><span class="sxs-lookup"><span data-stu-id="a69a6-221">COPY\_SOURCE</span></span>                  | <span data-ttu-id="a69a6-222">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-222">Yes</span></span>                                          | <span data-ttu-id="a69a6-223">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-223">Yes</span></span>                                  |
| <span data-ttu-id="a69a6-224">RISOLVERE \_ IL DEST</span><span class="sxs-lookup"><span data-stu-id="a69a6-224">RESOLVE\_DEST</span></span>                 | <span data-ttu-id="a69a6-225">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-225">Yes</span></span>                                          | <span data-ttu-id="a69a6-226">No</span><span class="sxs-lookup"><span data-stu-id="a69a6-226">No</span></span>                                   |
| <span data-ttu-id="a69a6-227">RISOLVERE \_ L'ORIGINE</span><span class="sxs-lookup"><span data-stu-id="a69a6-227">RESOLVE\_SOURCE</span></span>               | <span data-ttu-id="a69a6-228">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-228">Yes</span></span>                                          | <span data-ttu-id="a69a6-229">No</span><span class="sxs-lookup"><span data-stu-id="a69a6-229">No</span></span>                                   |
| <span data-ttu-id="a69a6-230">PREDICAZIONE</span><span class="sxs-lookup"><span data-stu-id="a69a6-230">PREDICATION</span></span>                   | <span data-ttu-id="a69a6-231">Sì</span><span class="sxs-lookup"><span data-stu-id="a69a6-231">Yes</span></span>                                          | <span data-ttu-id="a69a6-232">No</span><span class="sxs-lookup"><span data-stu-id="a69a6-232">No</span></span>                                   |



 

<span data-ttu-id="a69a6-233"><sup>\*</sup>Le risorse depth-stencil devono essere trame di accesso non simultanee e pertanto non possono mai essere promosse in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="a69a6-233"><sup>\*</sup>Depth-stencil resources must be non-simultaneous-access textures and thus can never be implicitly promoted.</span></span>

<span data-ttu-id="a69a6-234">Quando si verifica questo accesso, la promozione agisce come una barriera di risorse implicita.</span><span class="sxs-lookup"><span data-stu-id="a69a6-234">When this access occurs the promotion acts like an implicit resource barrier.</span></span> <span data-ttu-id="a69a6-235">Per gli accessi successivi, sarà necessario modificare lo stato della risorsa, se necessario.</span><span class="sxs-lookup"><span data-stu-id="a69a6-235">For subsequent accesses, resource barriers will be required to change the resource state if necessary.</span></span> <span data-ttu-id="a69a6-236">Si noti che la promozione da uno stato di lettura promosso a più stati di lettura è valida, ma questo non è il caso degli stati di scrittura.</span><span class="sxs-lookup"><span data-stu-id="a69a6-236">Note that promotion from one promoted read state into multiple read state is valid, but this is not the case for write states.</span></span>  
<span data-ttu-id="a69a6-237">Ad esempio, se una risorsa nello stato comune viene promossa a RISORSA PIXEL SHADER in una chiamata draw, può comunque essere promossa a NON_PIXEL \_ \_ RISORSA SHADER \_ \_ | RISORSA PIXEL \_ SHADER \_ in un'altra chiamata draw.</span><span class="sxs-lookup"><span data-stu-id="a69a6-237">For example, if a resource in the common state is promoted to PIXEL\_SHADER\_RESOURCE in a Draw call, it can still be promoted to NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE in another Draw call.</span></span> <span data-ttu-id="a69a6-238">Tuttavia, se viene usato in un'operazione di scrittura, ad esempio una destinazione di copia, una barriera di transizione dello stato della risorsa dagli stati di lettura alzati di livello combinati, NON_PIXEL \_ SHADER \_ RESOURCE | RISORSA PIXEL \_ \_ SHADER, per \_ copiare DEST è necessario.</span><span class="sxs-lookup"><span data-stu-id="a69a6-238">However, if it is used in a write operation, such as a copy destination, a resource state transition barrier from the combined promoted read states, here NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE, to COPY\_DEST is needed.</span></span>  
<span data-ttu-id="a69a6-239">Analogamente, se promosso da COMMON a COPY DEST, è comunque necessario un ostacolo per la transizione da \_ COPY \_ DEST a RENDER \_ TARGET.</span><span class="sxs-lookup"><span data-stu-id="a69a6-239">Similarly, if promoted from COMMON to COPY\_DEST, a barrier is still required to transition from COPY\_DEST to RENDER\_TARGET.</span></span>

<span data-ttu-id="a69a6-240">Si noti che la promozione dello stato comune è "gratuita" perché la GPU non deve eseguire attese di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="a69a6-240">Note that common state promotion is "free" in that there is no need for the GPU to perform any synchronization waits.</span></span> <span data-ttu-id="a69a6-241">La promozione rappresenta il fatto che le risorse nello stato COMMON non devono richiedere operazioni aggiuntive sulla GPU o sul rilevamento dei driver per supportare determinati accessi.</span><span class="sxs-lookup"><span data-stu-id="a69a6-241">The promotion represents the fact that resources in the COMMON state should not require additional GPU work or driver tracking to support certain accesses.</span></span>

### <a name="state-decay-to-common"></a><span data-ttu-id="a69a6-242">Decadimento dello stato a comune</span><span class="sxs-lookup"><span data-stu-id="a69a6-242">State decay to common</span></span>

<span data-ttu-id="a69a6-243">Il lato opposto della promozione dello stato comune è il decadimento a D3D12 \_ RESOURCE \_ STATE \_ COMMON.</span><span class="sxs-lookup"><span data-stu-id="a69a6-243">The flip-side of common state promotion is decay back to D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="a69a6-244">Le risorse che soddisfano determinati requisiti sono considerate senza stato e tornano effettivamente allo stato comune quando la GPU termina l'esecuzione di [**un'operazione ExecuteCommandLists.**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)</span><span class="sxs-lookup"><span data-stu-id="a69a6-244">Resources that meet certain requirements are considered to be stateless and effectively return to the common state when the GPU finishes execution of an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation.</span></span> <span data-ttu-id="a69a6-245">Il decadimento non si verifica tra gli elenchi di comandi eseguiti insieme nella stessa **chiamata a ExecuteCommandLists.**</span><span class="sxs-lookup"><span data-stu-id="a69a6-245">Decay does not occur between command lists executed together in the same **ExecuteCommandLists** call.</span></span>

<span data-ttu-id="a69a6-246">Quando un'operazione [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) viene completata nella GPU, le risorse seguenti verranno decadimento:</span><span class="sxs-lookup"><span data-stu-id="a69a6-246">The following resources will decay when an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation is completed on the GPU:</span></span>

-   <span data-ttu-id="a69a6-247">Risorse a cui si accede in una coda di copia *o*</span><span class="sxs-lookup"><span data-stu-id="a69a6-247">Resources being accessed on a Copy queue, *or*</span></span>
-   <span data-ttu-id="a69a6-248">Buffer delle risorse in qualsiasi tipo di coda *o*</span><span class="sxs-lookup"><span data-stu-id="a69a6-248">Buffer resources on any queue type, *or*</span></span>
-   <span data-ttu-id="a69a6-249">Risorse di trama in qualsiasi tipo di coda per cui è impostato il flag DI RISORSA D3D12 \_ \_ ALLOW SIMULTANEOUS ACCESS \_ \_ \_ *oppure*</span><span class="sxs-lookup"><span data-stu-id="a69a6-249">Texture resources on any queue type that have the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set, *or*</span></span>
-   <span data-ttu-id="a69a6-250">Qualsiasi risorsa promossa in modo implicito a uno stato di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a69a6-250">Any resource implicitly promoted to a read-only state.</span></span>

<span data-ttu-id="a69a6-251">Come la promozione dello stato comune, il decadimento è gratuito perché non è necessaria alcuna sincronizzazione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="a69a6-251">Like common state promotion, the decay is free in that no additional synchronization is needed.</span></span> <span data-ttu-id="a69a6-252">La combinazione di promozione e decadimento comuni dello stato consente di eliminare molte [**transizioni resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) non necessarie.</span><span class="sxs-lookup"><span data-stu-id="a69a6-252">Combining common state promotion and decay can help to eliminate many unnecessary [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions.</span></span> <span data-ttu-id="a69a6-253">In alcuni casi, ciò può offrire miglioramenti significativi delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a69a6-253">In some cases, this can provide significant performance improvements.</span></span>

<span data-ttu-id="a69a6-254">I buffer e Simultaneous-Access risorse verranno decadimento allo stato comune indipendentemente dal fatto che siano state esplicitamente transizionate usando barriere di risorse o promosse in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="a69a6-254">Buffers and Simultaneous-Access resources will decay to the common state regardless of whether they were explicitly transitioned using resource barriers or implicitly promoted.</span></span>

### <a name="performance-implications"></a><span data-ttu-id="a69a6-255">Implicazioni per le prestazioni</span><span class="sxs-lookup"><span data-stu-id="a69a6-255">Performance implications</span></span>

<span data-ttu-id="a69a6-256">Quando si registrano transizioni esplicite di [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) sulle risorse nello stato comune, è corretto usare D3D12 RESOURCE STATE COMMON o qualsiasi stato promobile come valore BeforeState nella struttura \_ \_ \_ D3D12 RESOURCE TRANSITION  \_ \_ \_ BARRIER.</span><span class="sxs-lookup"><span data-stu-id="a69a6-256">When recording explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions on resources in the common state, it is correct to use either D3D12\_RESOURCE\_STATE\_COMMON or any promotable state as the *BeforeState* value in the D3D12\_RESOURCE\_TRANSITION\_BARRIER structure.</span></span> <span data-ttu-id="a69a6-257">Ciò consente la gestione dello stato tradizionale che ignora il decadimento automatico dei buffer e delle trame ad accesso simultaneo.</span><span class="sxs-lookup"><span data-stu-id="a69a6-257">This allows traditional state management that ignores automatic decay of buffers and simultaneous-access textures.</span></span> <span data-ttu-id="a69a6-258">Questo potrebbe non essere consigliabile, tuttavia, poiché evitare chiamate **ResourceBarrier** di transizione con risorse note allo stato comune può migliorare significativamente le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a69a6-258">This may not be desirable though, as avoiding transition **ResourceBarrier** calls with resources known to be in the common state can significantly improve performance.</span></span> <span data-ttu-id="a69a6-259">Le barriere delle risorse possono essere costose.</span><span class="sxs-lookup"><span data-stu-id="a69a6-259">Resource barriers can be expensive.</span></span> <span data-ttu-id="a69a6-260">Sono progettate per forzare lo scaricamento della cache, le modifiche al layout della memoria e altre operazioni di sincronizzazione che potrebbero non essere necessarie per le risorse già in stato comune.</span><span class="sxs-lookup"><span data-stu-id="a69a6-260">They are designed to force cache flushes, memory layout changes and other synchronization that may not be necessary for resources already in the common state.</span></span> <span data-ttu-id="a69a6-261">Un elenco di comandi che usa una barriera di risorse da uno stato non comune a un altro stato non comune in una risorsa attualmente nello stato comune può introdurre un sovraccarico non necessario.</span><span class="sxs-lookup"><span data-stu-id="a69a6-261">A command list that uses a resource barrier from a non-common state to another non-common state on a resource currently in the common state can introduce a lot of unneeded overhead.</span></span>

<span data-ttu-id="a69a6-262">Evitare inoltre transizioni esplicite di [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) a D3D12 RESOURCE STATE COMMON a meno che non sia assolutamente necessario \_ (ad esempio, l'accesso successivo si trova in una coda di comandi COPY che richiede che le risorse inizino \_ \_ nello stato comune).</span><span class="sxs-lookup"><span data-stu-id="a69a6-262">Also, avoid explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions to D3D12\_RESOURCE\_STATE\_COMMON unless absolutely necessary (e.g. the next access is on a COPY command queue which requires a resources begin in the common state).</span></span> <span data-ttu-id="a69a6-263">Le transizioni eccessive allo stato comune possono rallentare notevolmente le prestazioni della GPU.</span><span class="sxs-lookup"><span data-stu-id="a69a6-263">Excessive transitions to the common state can dramatically slow down GPU performance.</span></span>

<span data-ttu-id="a69a6-264">In breve, provare a fare affidamento sulla promozione dello stato comune e decadimento ogni volta che la semantica consente di uscire senza emettere chiamate [**a ResourceBarrier.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)</span><span class="sxs-lookup"><span data-stu-id="a69a6-264">In summary, try to rely on common state promotion and decay whenever its semantics let you get away without issuing [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) calls.</span></span>

## <a name="split-barriers"></a><span data-ttu-id="a69a6-265">Dividere le barriere</span><span class="sxs-lookup"><span data-stu-id="a69a6-265">Split Barriers</span></span>

<span data-ttu-id="a69a6-266">Una barriera di transizione della risorsa con il flag D3D12 RESOURCE BARRIER FLAG BEGIN ONLY avvia una barriera di divisione e la barriera di transizione viene \_ \_ detto in \_ \_ \_ sospeso.</span><span class="sxs-lookup"><span data-stu-id="a69a6-266">A resource transition barrier with the D3D12\_RESOURCE\_BARRIER\_FLAG\_BEGIN\_ONLY flag begins a split barrier and the transition barrier is said to be pending.</span></span> <span data-ttu-id="a69a6-267">Mentre la barriera è in sospeso, la risorsa (secondaria) non può essere letta o scritta dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="a69a6-267">While the barrier is pending the (sub)resource cannot be read or written by the GPU.</span></span> <span data-ttu-id="a69a6-268">L'unica barriera di transizione legale che può essere applicata a una risorsa  (secondaria) con una barriera in sospeso è una con gli stessi stati *prima* e dopo e il flag D3D12 RESOURCE BARRIER FLAG END ONLY, che consente di completare la transizione in \_ \_ \_ \_ \_ sospeso.</span><span class="sxs-lookup"><span data-stu-id="a69a6-268">The only legal transition barrier that can be applied to a (sub)resource with a pending barrier is one with the same *before* and *after* states and the D3D12\_RESOURCE\_BARRIER\_FLAG\_END\_ONLY flag, which barrier completes the pending transition.</span></span>

<span data-ttu-id="a69a6-269">Le barriere di divisione forniscono suggerimenti alla GPU che una risorsa nello stato *A* verrà usata successivamente nello stato *B.*</span><span class="sxs-lookup"><span data-stu-id="a69a6-269">Split barriers provide hints to the GPU that a resource in state *A* will next be used in state *B* sometime later.</span></span> <span data-ttu-id="a69a6-270">In questo modo la GPU può ottimizzare il carico di lavoro di transizione, riducendo o eliminando i blocchi di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a69a6-270">This gives the GPU the option to optimize the transition workload, possibly reducing or eliminating execution stalls.</span></span> <span data-ttu-id="a69a6-271">L'emissione della barriera end-only garantisce che tutte le operazioni di transizione gpu vengono completate prima di passare al comando successivo.</span><span class="sxs-lookup"><span data-stu-id="a69a6-271">Issuing the end-only barrier guarantees that all GPU transition work is finished before moving onto the next command.</span></span>

<span data-ttu-id="a69a6-272">L'uso di barriere di divisione può contribuire a migliorare le prestazioni, in particolare in scenari con più motori o in cui le risorse sono in fase di transizione in lettura/scrittura in uno o più elenchi di comandi.</span><span class="sxs-lookup"><span data-stu-id="a69a6-272">Using split barriers can help to improve performance, especially in multi-engine scenarios or where resources are read/write transitioned sparsely throughout one or more command lists.</span></span>

## <a name="resource-barrier-example-scenario"></a><span data-ttu-id="a69a6-273">Scenario di esempio di barriera delle risorse</span><span class="sxs-lookup"><span data-stu-id="a69a6-273">Resource barrier example scenario</span></span>

<span data-ttu-id="a69a6-274">I frammenti di codice seguenti illustrano l'uso [**del metodo ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) in un esempio di multithreading.</span><span class="sxs-lookup"><span data-stu-id="a69a6-274">The following snippets show the use of the [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) method in a multi-threading sample.</span></span>

<span data-ttu-id="a69a6-275">Creazione della depth stencil, transizione a uno stato scrivibile.</span><span class="sxs-lookup"><span data-stu-id="a69a6-275">Creating the depth stencil view, transitioning it to a writeable state.</span></span>


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



<span data-ttu-id="a69a6-276">Creazione della visualizzazione del buffer dei vertici, prima di tutto da uno stato comune a uno di destinazione e quindi da una destinazione a uno stato leggibile generico.</span><span class="sxs-lookup"><span data-stu-id="a69a6-276">Creating the vertex buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



<span data-ttu-id="a69a6-277">Creazione della index buffer, prima di tutto da uno stato comune a uno di destinazione e quindi da una destinazione a uno stato leggibile generico.</span><span class="sxs-lookup"><span data-stu-id="a69a6-277">Creating the index buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



<span data-ttu-id="a69a6-278">Creazione di trame e visualizzazioni delle risorse shader.</span><span class="sxs-lookup"><span data-stu-id="a69a6-278">Creating textures and shader resource views.</span></span> <span data-ttu-id="a69a6-279">La trama viene modificata da uno stato comune a una destinazione e quindi da una destinazione a una pixel shader risorsa.</span><span class="sxs-lookup"><span data-stu-id="a69a6-279">The texture is changed from a common state to a destination, and then from a destination to a pixel shader resource.</span></span>


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



<span data-ttu-id="a69a6-280">Inizio di un frame; non solo usa [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) per indicare che il buffer nascosto deve essere usato come destinazione di rendering, ma inizializza anche la risorsa frame (che chiama **ResourceBarrier** sul buffer depth stencil).</span><span class="sxs-lookup"><span data-stu-id="a69a6-280">Beginning a frame; this not only uses [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to indicate that the backbuffer is to be used as a render target, but also initializes the frame resource (which calls **ResourceBarrier** on the depth stencil buffer).</span></span>


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



<span data-ttu-id="a69a6-281">Terminazione di un frame, che indica che il buffer nascosto viene ora usato per la presentazione.</span><span class="sxs-lookup"><span data-stu-id="a69a6-281">Ending a frame, indicating the back buffer is now used to present.</span></span>


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



<span data-ttu-id="a69a6-282">L'inizializzazione di una risorsa frame, chiamata all'inizio di un frame, esegue la transizione depth stencil buffer a scrivibile.</span><span class="sxs-lookup"><span data-stu-id="a69a6-282">Initializing a frame resource, called when beginning a frame, transitions the depth stencil buffer to writeable.</span></span>


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



<span data-ttu-id="a69a6-283">Le barriere vengono scambiate nel fotogramma intermedio, con la transizione della mappa ombreggiatura da scrivibile a leggibile.</span><span class="sxs-lookup"><span data-stu-id="a69a6-283">Barriers are swapped mid-frame, transitioning the shadow map from writeable to readable.</span></span>


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



<span data-ttu-id="a69a6-284">Il metodo Finish viene chiamato al termine di un frame, con la transizione della mappa ombreggiatura a uno stato comune.</span><span class="sxs-lookup"><span data-stu-id="a69a6-284">Finish is called when a frame is ended, transitioning the shadow map to a common state.</span></span>


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a><span data-ttu-id="a69a6-285">Esempio comune di promozione e decadimento dello stato</span><span class="sxs-lookup"><span data-stu-id="a69a6-285">Common state promotion and decay sample</span></span>

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a><span data-ttu-id="a69a6-286">Esempio di barriere di divisione</span><span class="sxs-lookup"><span data-stu-id="a69a6-286">Example of split barriers</span></span>

<span data-ttu-id="a69a6-287">L'esempio seguente illustra come usare una barriera di divisione per ridurre i blocchi della pipeline.</span><span class="sxs-lookup"><span data-stu-id="a69a6-287">The following example shows how to use a split barrier to reduce pipeline stalls.</span></span> <span data-ttu-id="a69a6-288">Il codice seguente non usa barriere di divisione:</span><span class="sxs-lookup"><span data-stu-id="a69a6-288">The code that follows does not use split barriers:</span></span>

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

<span data-ttu-id="a69a6-289">Il codice seguente usa le barriere di divisione:</span><span class="sxs-lookup"><span data-stu-id="a69a6-289">The following code uses split barriers:</span></span>

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a><span data-ttu-id="a69a6-290">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a69a6-290">Related topics</span></span>

[<span data-ttu-id="a69a6-291">Esercitazioni video sull'apprendimento avanzato di DirectX: Barriere delle risorse e rilevamento dello stato</span><span class="sxs-lookup"><span data-stu-id="a69a6-291">DirectX advanced learning video tutorials : Resource Barriers and State Tracking</span></span>](https://www.youtube.com/watch?v=nmB2XMasz2o)

[<span data-ttu-id="a69a6-292">Sincronizzazione di più motori</span><span class="sxs-lookup"><span data-stu-id="a69a6-292">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)

[<span data-ttu-id="a69a6-293">Invio di lavoro in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a69a6-293">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)

[<span data-ttu-id="a69a6-294">Uno sguardo all'interno delle barriere dello stato delle risorse D3D12</span><span class="sxs-lookup"><span data-stu-id="a69a6-294">A Look Inside D3D12 Resource State Barriers</span></span>](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

