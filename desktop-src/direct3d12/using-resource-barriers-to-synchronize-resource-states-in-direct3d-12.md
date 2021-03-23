---
title: Uso delle barriere delle risorse per sincronizzare gli Stati delle risorse in Direct3D 12
description: Per ridurre l'utilizzo complessivo della CPU e consentire il multithreading e la pre-elaborazione dei driver, Direct3D 12 sposta la responsabilità della gestione dello stato per ogni risorsa dal driver di grafica all'applicazione.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c766f18e85ab8acc2ed0afad8e680d566a723a68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104548885"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a><span data-ttu-id="ad877-103">Uso delle barriere delle risorse per sincronizzare gli Stati delle risorse in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="ad877-103">Using Resource Barriers to Synchronize Resource States in Direct3D 12</span></span>

<span data-ttu-id="ad877-104">Per ridurre l'utilizzo complessivo della CPU e consentire il multithreading e la pre-elaborazione dei driver, Direct3D 12 sposta la responsabilità della gestione dello stato per ogni risorsa dal driver di grafica all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ad877-104">To reduce overall CPU usage and enable driver multi-threading and pre-processing, Direct3D 12 moves the responsibility of per-resource state management from the graphics driver to the application.</span></span> <span data-ttu-id="ad877-105">Un esempio di stato per risorsa è se è attualmente possibile accedere a una risorsa di trama come tramite un Shader Resource View o come una visualizzazione di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="ad877-105">An example of per-resource state is whether a texture resource is currently being accessed as through a Shader Resource View or as a Render Target View.</span></span> <span data-ttu-id="ad877-106">In Direct3D 11 i driver sono necessari per tenere traccia di questo stato in background.</span><span class="sxs-lookup"><span data-stu-id="ad877-106">In Direct3D 11, drivers were required to track this state in the background.</span></span> <span data-ttu-id="ad877-107">Si tratta di un'operazione dispendiosa dal punto di vista della CPU e complica notevolmente qualsiasi tipo di progettazione multithread.</span><span class="sxs-lookup"><span data-stu-id="ad877-107">This is expensive from a CPU perspective and significantly complicates any sort of multi-threaded design.</span></span> <span data-ttu-id="ad877-108">In Microsoft Direct3D 12 la maggior parte dello stato per ogni risorsa viene gestita dall'applicazione con una singola API, [**ID3D12GraphicsCommandList:: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="ad877-108">In Microsoft Direct3D 12, most per-resource state is managed by the application with a single API, [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>

-   [<span data-ttu-id="ad877-109">Uso dell'API ResourceBarrier per gestire lo stato per risorsa</span><span class="sxs-lookup"><span data-stu-id="ad877-109">Using the ResourceBarrier API to manage per-resource state</span></span>](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [<span data-ttu-id="ad877-110">Stati delle risorse</span><span class="sxs-lookup"><span data-stu-id="ad877-110">Resource states</span></span>](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [<span data-ttu-id="ad877-111">Stati iniziali per le risorse</span><span class="sxs-lookup"><span data-stu-id="ad877-111">Initial states for resources</span></span>](#initial-states-for-resources)
    -   [<span data-ttu-id="ad877-112">Restrizioni sullo stato delle risorse di lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ad877-112">Read/write resource state restrictions</span></span>](#readwrite-resource-state-restrictions)
    -   [<span data-ttu-id="ad877-113">Stati delle risorse per la presentazione dei buffer indietro</span><span class="sxs-lookup"><span data-stu-id="ad877-113">Resource states for presenting back buffers</span></span>](#resource-states-for-presenting-back-buffers)
    -   [<span data-ttu-id="ad877-114">Eliminazione di risorse</span><span class="sxs-lookup"><span data-stu-id="ad877-114">Discarding resources</span></span>](#discarding-resources)
-   [<span data-ttu-id="ad877-115">Transizioni di stato implicite</span><span class="sxs-lookup"><span data-stu-id="ad877-115">Implicit State Transitions</span></span>](#implicit-state-transitions)
    -   [<span data-ttu-id="ad877-116">Innalzamento di stato comune</span><span class="sxs-lookup"><span data-stu-id="ad877-116">Common state promotion</span></span>](#common-state-promotion)
    -   [<span data-ttu-id="ad877-117">Stato decadimento in comune</span><span class="sxs-lookup"><span data-stu-id="ad877-117">State decay to common</span></span>](#state-decay-to-common)
    -   [<span data-ttu-id="ad877-118">Implicazioni per le prestazioni</span><span class="sxs-lookup"><span data-stu-id="ad877-118">Performance implications</span></span>](#performance-implications)
-   [<span data-ttu-id="ad877-119">Suddividere le barriere</span><span class="sxs-lookup"><span data-stu-id="ad877-119">Split Barriers</span></span>](#split-barriers)
-   [<span data-ttu-id="ad877-120">Scenario di esempio di barriera delle risorse</span><span class="sxs-lookup"><span data-stu-id="ad877-120">Resource barrier example scenario</span></span>](#resource-barrier-example-scenario)
-   [<span data-ttu-id="ad877-121">Esempio di promozione e decadimento dello stato comune</span><span class="sxs-lookup"><span data-stu-id="ad877-121">Common state promotion and decay sample</span></span>](#common-state-promotion-and-decay-sample)
-   [<span data-ttu-id="ad877-122">Esempio di barriere Split</span><span class="sxs-lookup"><span data-stu-id="ad877-122">Example of split barriers</span></span>](#example-of-split-barriers)
-   [<span data-ttu-id="ad877-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad877-123">Related topics</span></span>](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a><span data-ttu-id="ad877-124">Uso dell'API ResourceBarrier per gestire lo stato per risorsa</span><span class="sxs-lookup"><span data-stu-id="ad877-124">Using the ResourceBarrier API to manage per-resource state</span></span>

<span data-ttu-id="ad877-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifica al driver Graphics le situazioni in cui il driver potrebbe dover sincronizzare più accessi alla memoria in cui è archiviata una risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad877-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifies the graphics driver of situations in which the driver may need to synchronize multiple accesses to the memory in which a resource is stored.</span></span> <span data-ttu-id="ad877-126">Il metodo viene chiamato con una o più strutture di descrizione della barriera delle risorse che indicano il tipo di barriera della risorsa dichiarata.</span><span class="sxs-lookup"><span data-stu-id="ad877-126">The method is called with one or more resource barrier description structures indicating the type of resource barrier being declared.</span></span>

<span data-ttu-id="ad877-127">Esistono tre tipi di barriere per le risorse:</span><span class="sxs-lookup"><span data-stu-id="ad877-127">There are three types of resource barriers:</span></span>

-   <span data-ttu-id="ad877-128">**Barriera di transizione** : una barriera di transizione indica che un set di sottorisorse viene sottoposto a transizione tra diversi usi.</span><span class="sxs-lookup"><span data-stu-id="ad877-128">**Transition barrier** - A transition barrier indicates that a set of subresources transition between different usages.</span></span> <span data-ttu-id="ad877-129">Una struttura della [**\_ \_ \_ barriera di transizione delle risorse D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) viene utilizzata per specificare la sottorisorsa che esegue la transizione, nonché gli stati *before* e *after* della sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="ad877-129">A [**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) structure is used to specify the subresource that is transitioning as well as the *before* and *after* states of the subresource.</span></span>

    <span data-ttu-id="ad877-130">Il sistema verifica che le transizioni delle sottorisorse in un elenco di comandi siano coerenti con le transizioni precedenti nello stesso elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="ad877-130">The system verifies that subresource transitions in a command list are consistent with previous transitions in the same command list.</span></span> <span data-ttu-id="ad877-131">Il livello di debug rileva ulteriormente lo stato della sottorisorsa per trovare altri errori, tuttavia questa convalida è conservativa e non esaustiva.</span><span class="sxs-lookup"><span data-stu-id="ad877-131">The debug layer further tracks subresource state to find other errors however this validation is conservative and not exhaustive.</span></span>

    <span data-ttu-id="ad877-132">Si noti che è possibile usare il \_ flag D3D12 Resource \_ Barrier \_ All \_ Resources per specificare che tutte le sottorisorse all'interno di una risorsa sono in fase di transizione.</span><span class="sxs-lookup"><span data-stu-id="ad877-132">Note that you can use the D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES flag to specify that all subresources within a resource are being transitioned.</span></span>

-   <span data-ttu-id="ad877-133">**Barriera di alias** : una barriera di aliasing indica una transizione tra gli utilizzi di due risorse diverse con mapping sovrapposti nello stesso heap.</span><span class="sxs-lookup"><span data-stu-id="ad877-133">**Aliasing barrier** - An aliasing barrier indicates a transition between usages of two different resources which have overlapping mappings into the same heap.</span></span> <span data-ttu-id="ad877-134">Questo vale sia per le risorse riservate che per quelle posizionate.</span><span class="sxs-lookup"><span data-stu-id="ad877-134">This applies to both reserved and placed resources.</span></span> <span data-ttu-id="ad877-135">Una struttura di barriera per l' [**\_ \_ aliasing \_ delle risorse D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) viene usata per specificare sia la risorsa *before* che la risorsa *after* .</span><span class="sxs-lookup"><span data-stu-id="ad877-135">A [**D3D12\_RESOURCE\_ALIASING\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) structure is used to specify both the *before* resource and the *after* resource.</span></span>

    <span data-ttu-id="ad877-136">Si noti che una o entrambe le risorse possono essere NULL, a indicare che qualsiasi risorsa affiancata potrebbe causare l'aliasing.</span><span class="sxs-lookup"><span data-stu-id="ad877-136">Note that one or both resources can be NULL, which indicates that any tiled resource could cause aliasing.</span></span> <span data-ttu-id="ad877-137">Per ulteriori informazioni sull'utilizzo di risorse affiancate, vedere [risorse affiancate](../direct3d11/tiled-resources.md) e [risorse affiancate al volume](volume-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="ad877-137">For more information about using tiled resources, see [Tiled resources](../direct3d11/tiled-resources.md) and [Volume Tiled Resources](volume-tiled-resources.md).</span></span>

-   <span data-ttu-id="ad877-138">**Barriera di visualizzazione di accesso non ordinato (UAV)** : una barriera UAV indica che tutti gli accessi UAV, sia di lettura che di scrittura, a una determinata risorsa devono essere completati tra gli accessi UAV futuri, sia di lettura che di scrittura.</span><span class="sxs-lookup"><span data-stu-id="ad877-138">**Unordered access view (UAV) barrier** - A UAV barrier indicates that all UAV accesses, both read or write, to a particular resource must complete between any future UAV accesses, both read or write.</span></span> <span data-ttu-id="ad877-139">Non è necessario che un'app inserisca una barriera UAV tra due chiamate di estrazione o di invio che leggono solo da un UAV.</span><span class="sxs-lookup"><span data-stu-id="ad877-139">It's not necessary for an app to put a UAV barrier between two draw or dispatch calls that only read from a UAV.</span></span> <span data-ttu-id="ad877-140">Non è inoltre necessario inserire una barriera UAV tra due chiamate di richiamo o di invio che scrivono nello stesso UAV se l'applicazione sa che è sicuro eseguire l'accesso UAV in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="ad877-140">Also, it's not necessary to put a UAV barrier between two draw or dispatch calls that write to the same UAV if the application knows that it is safe to execute the UAV access in any order.</span></span> <span data-ttu-id="ad877-141">Per specificare la risorsa UAV a cui si applica la barriera, viene usata una struttura di [**\_ \_ \_ barriera UAV della risorsa D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) .</span><span class="sxs-lookup"><span data-stu-id="ad877-141">A [**D3D12\_RESOURCE\_UAV\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) structure is used to specify the UAV resource to which the barrier applies.</span></span> <span data-ttu-id="ad877-142">L'applicazione può specificare NULL per il UAV della barriera, che indica che qualsiasi accesso UAV potrebbe richiedere la barriera.</span><span class="sxs-lookup"><span data-stu-id="ad877-142">The application can specify NULL for the barrier's UAV, which indicates that any UAV access could require the barrier.</span></span>

<span data-ttu-id="ad877-143">Quando [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) viene chiamato con una matrice di descrizioni della barriera delle risorse, l'API si comporta come se venisse chiamata una volta per ogni elemento, nell'ordine in cui sono state specificate.</span><span class="sxs-lookup"><span data-stu-id="ad877-143">When [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) is called with an array of resource barrier descriptions, the API behaves as if it was called once for each element, in the order in which they were supplied.</span></span>

<span data-ttu-id="ad877-144">In un determinato momento, una sottorisorsa si trova esattamente in uno stato, determinato dal set di flag di stato [**\_ delle risorse \_ D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) forniti a [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="ad877-144">At any given time, a subresource is in exactly one state, determined by the set of [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) flags supplied to [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span> <span data-ttu-id="ad877-145">L'applicazione deve garantire che gli stati *before* e *after* delle chiamate consecutive a **ResourceBarrier** accettino.</span><span class="sxs-lookup"><span data-stu-id="ad877-145">The application must ensure that the *before* and *after* states of consecutive calls to **ResourceBarrier** agree.</span></span>

> [!TIP]
>
> <span data-ttu-id="ad877-146">Le applicazioni devono eseguire il batch di più transizioni in una chiamata API laddove possibile.</span><span class="sxs-lookup"><span data-stu-id="ad877-146">Applications should batch multiple transitions into one API call wherever possible.</span></span>

 

### <a name="resource-states"></a><span data-ttu-id="ad877-147">Stati delle risorse</span><span class="sxs-lookup"><span data-stu-id="ad877-147">Resource states</span></span>

<span data-ttu-id="ad877-148">Per l'elenco completo degli Stati delle risorse tra cui una risorsa può passare, vedere l'argomento di riferimento per l'enumerazione [**\_ \_ degli Stati delle risorse D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .</span><span class="sxs-lookup"><span data-stu-id="ad877-148">For the complete list of resource states that a resource can transition between, see the reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) enumeration.</span></span>

<span data-ttu-id="ad877-149">Per le barriere Split Resource, vedere [**anche \_ \_ \_ flag di barriera delle risorse D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span><span class="sxs-lookup"><span data-stu-id="ad877-149">For split resource barriers, also refer to [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span></span>

### <a name="initial-states-for-resources"></a><span data-ttu-id="ad877-150">Stati iniziali per le risorse</span><span class="sxs-lookup"><span data-stu-id="ad877-150">Initial states for resources</span></span>

<span data-ttu-id="ad877-151">Le risorse possono essere create con qualsiasi stato iniziale specificato dall'utente (valido per la descrizione della risorsa), con le eccezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ad877-151">Resources may be created with any user-specified initial state (valid for the resource description), with the following exceptions:</span></span>

-   <span data-ttu-id="ad877-152">Gli heap di caricamento devono iniziare con lo stato della \_ risorsa \_ D3D12 \_ lettura generica \_ , che è una combinazione OR bit per bit di:</span><span class="sxs-lookup"><span data-stu-id="ad877-152">Upload heaps must start out in the state D3D12\_RESOURCE\_STATE\_GENERIC\_READ which is a bitwise OR combination of:</span></span>
    -   <span data-ttu-id="ad877-153">\_ \_ Vertex dello stato della risorsa D3D12 \_ \_ e \_ \_ buffer costante</span><span class="sxs-lookup"><span data-stu-id="ad877-153">D3D12\_RESOURCE\_STATE\_VERTEX\_AND\_CONSTANT\_BUFFER</span></span>
    -   <span data-ttu-id="ad877-154">\_ \_ \_ Buffer indice stato risorsa \_ D3D12</span><span class="sxs-lookup"><span data-stu-id="ad877-154">D3D12\_RESOURCE\_STATE\_INDEX\_BUFFER</span></span>
    -   <span data-ttu-id="ad877-155">\_Origine della \_ copia dello stato della risorsa \_ D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="ad877-155">D3D12\_RESOURCE\_STATE\_COPY\_SOURCE</span></span>
    -   <span data-ttu-id="ad877-156">\_ \_ Risorsa dello stato della risorsa \_ non \_ pixel \_ shader \_ di D3D12</span><span class="sxs-lookup"><span data-stu-id="ad877-156">D3D12\_RESOURCE\_STATE\_NON\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="ad877-157">\_ \_ \_ \_ Risorsa pixel shader dello stato della risorsa D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="ad877-157">D3D12\_RESOURCE\_STATE\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="ad877-158">\_ \_ \_ Argomento indiretto dello stato della risorsa D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="ad877-158">D3D12\_RESOURCE\_STATE\_INDIRECT\_ARGUMENT</span></span>
-   <span data-ttu-id="ad877-159">Gli heap readback devono iniziare nello stato di \_ \_ copia dello stato della risorsa D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ad877-159">Readback heaps must start out in the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span>
-   <span data-ttu-id="ad877-160">I buffer indietro della catena di scambio iniziano automaticamente nello \_ stato comune della risorsa D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ad877-160">Swap chain back buffers automatically start out in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span>

<span data-ttu-id="ad877-161">Prima che un heap possa essere la destinazione di un'operazione di copia GPU, in genere l'heap deve prima essere passato allo \_ \_ stato di copia dello stato della risorsa D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ad877-161">Before a heap can be the target of a GPU copy operation, normally the heap must first be transitioned to the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span> <span data-ttu-id="ad877-162">Tuttavia, le risorse create negli heap di caricamento devono iniziare in e non possono essere modificate dallo \_ stato di lettura generico poiché solo la CPU eseguirà la scrittura.</span><span class="sxs-lookup"><span data-stu-id="ad877-162">However, resources created on UPLOAD heaps must start in and cannot change from the GENERIC\_READ state since only the CPU will be doing writing.</span></span> <span data-ttu-id="ad877-163">Viceversa, le risorse di cui è stato eseguito il commit create negli heap READBACK devono iniziare da e non possono essere modificate dallo stato di copia \_ dest.</span><span class="sxs-lookup"><span data-stu-id="ad877-163">Conversely, committed resources created in READBACK heaps must start in and cannot change from the COPY\_DEST state.</span></span>

### <a name="readwrite-resource-state-restrictions"></a><span data-ttu-id="ad877-164">Restrizioni sullo stato delle risorse di lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ad877-164">Read/write resource state restrictions</span></span>

<span data-ttu-id="ad877-165">I bit di utilizzo dello stato delle risorse usati per descrivere lo stato di una risorsa sono divisi in Stati di sola lettura e di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ad877-165">The resource state usage bits that are used to describe a resource state are divided into read-only and read/write states.</span></span> <span data-ttu-id="ad877-166">L'argomento di riferimento per [**gli \_ \_ Stati della risorsa D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indica il livello di accesso in lettura/scrittura per ogni bit nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="ad877-166">The reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indicates the read/write access level for each bit in the enumeration.</span></span>

<span data-ttu-id="ad877-167">Al massimo, è possibile impostare un solo bit di lettura/scrittura per qualsiasi risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad877-167">At most, only one read/write bit can be set for any resource.</span></span> <span data-ttu-id="ad877-168">Se è impostato un bit di scrittura, non è possibile impostare alcun bit di sola lettura per tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad877-168">If a write bit is set, then no read-only bit may be set for that resource.</span></span> <span data-ttu-id="ad877-169">Se non è impostato alcun bit di scrittura, è possibile impostare un numero qualsiasi di bit di lettura.</span><span class="sxs-lookup"><span data-stu-id="ad877-169">If no write bit is set, then any number of read bits may be set.</span></span>

### <a name="resource-states-for-presenting-back-buffers"></a><span data-ttu-id="ad877-170">Stati delle risorse per la presentazione dei buffer indietro</span><span class="sxs-lookup"><span data-stu-id="ad877-170">Resource states for presenting back buffers</span></span>

<span data-ttu-id="ad877-171">Prima che venga visualizzato un buffer nascosto, questo deve trovarsi nello \_ stato comune della risorsa D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ad877-171">Before a back buffer is presented, it must be in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span> <span data-ttu-id="ad877-172">Si noti che lo stato della risorsa D3D12 stato \_ risorsa \_ \_ presente è un sinonimo di D3D12 \_ risorsa \_ stato \_ comune ed entrambi hanno un valore pari a 0.</span><span class="sxs-lookup"><span data-stu-id="ad877-172">Note, the resource state D3D12\_RESOURCE\_STATE\_PRESENT is a synonym for D3D12\_RESOURCE\_STATE\_COMMON, and they both have a value of 0.</span></span> <span data-ttu-id="ad877-173">Se [**IDXGISwapChain::P**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) reinviata (o [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) viene chiamato su una risorsa che non si trova attualmente in questo stato, viene generato un avviso di livello debug.</span><span class="sxs-lookup"><span data-stu-id="ad877-173">If [**IDXGISwapChain::Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (or [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) is called on a resource that is not currently in this state, a debug layer warning is emitted.</span></span>

### <a name="discarding-resources"></a><span data-ttu-id="ad877-174">Eliminazione di risorse</span><span class="sxs-lookup"><span data-stu-id="ad877-174">Discarding resources</span></span>

<span data-ttu-id="ad877-175">Tutte le sottorisorse in una risorsa devono trovarsi nello \_ stato di destinazione di rendering o \_ nello stato di scrittura di profondità, rispettivamente per le destinazioni di rendering o per le risorse dello stencil di profondità, quando viene chiamato [**ID3D12GraphicsCommandList::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) .</span><span class="sxs-lookup"><span data-stu-id="ad877-175">All subresources in a resource must be in the RENDER\_TARGET state, or DEPTH\_WRITE state, for render targets/depth-stencil resources respectively, when [**ID3D12GraphicsCommandList::DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) is called.</span></span>

## <a name="implicit-state-transitions"></a><span data-ttu-id="ad877-176">Transizioni di stato implicite</span><span class="sxs-lookup"><span data-stu-id="ad877-176">Implicit State Transitions</span></span>

<span data-ttu-id="ad877-177">Le risorse possono essere "promosse" solo dal \_ comune stato della risorsa D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ad877-177">Resources can only be "promoted" out of D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="ad877-178">Analogamente, le risorse risulteranno "decadimento" solo per \_ lo stato della risorsa D3D12 \_ \_ comune.</span><span class="sxs-lookup"><span data-stu-id="ad877-178">Similarly, resources will only "decay" to D3D12\_RESOURCE\_STATE\_COMMON.</span></span>

### <a name="common-state-promotion"></a><span data-ttu-id="ad877-179">Innalzamento di stato comune</span><span class="sxs-lookup"><span data-stu-id="ad877-179">Common state promotion</span></span>

<span data-ttu-id="ad877-180">Tutte le risorse del buffer e le trame con il \_ flag di risorsa D3D12 \_ consentono di impostare il \_ \_ \_ flag di accesso simultaneo in modo implicito dallo \_ stato della risorsa D3D12 \_ \_ comune allo stato pertinente per il primo accesso alla GPU, inclusa la lettura generica \_ per coprire qualsiasi scenario di lettura.</span><span class="sxs-lookup"><span data-stu-id="ad877-180">All buffer resources as well as textures with the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set are implicitly promoted from D3D12\_RESOURCE\_STATE\_COMMON to the relevant state on first GPU access, including GENERIC\_READ to cover any read scenario.</span></span> <span data-ttu-id="ad877-181">È possibile accedere a qualsiasi risorsa nello stato comune in un unico stato con</span><span class="sxs-lookup"><span data-stu-id="ad877-181">Any resource in the COMMON state can be accessed as through it were in a single state with</span></span>

<dl> <span data-ttu-id="ad877-182">1 flag di scrittura o</span><span class="sxs-lookup"><span data-stu-id="ad877-182">1 WRITE flag, or</span></span>  
<span data-ttu-id="ad877-183">uno o più flag di lettura</span><span class="sxs-lookup"><span data-stu-id="ad877-183">1 or more READ flags</span></span>  
</dl>

<span data-ttu-id="ad877-184">Le risorse possono essere promosse dallo stato comune in base alla tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="ad877-184">Resources can be promoted from the COMMON state based on the following table:</span></span>



| <span data-ttu-id="ad877-185">Flag di stato</span><span class="sxs-lookup"><span data-stu-id="ad877-185">State flag</span></span>                    | <span data-ttu-id="ad877-186">Stato promuovibile</span><span class="sxs-lookup"><span data-stu-id="ad877-186">Promotable State</span></span>                             |                                      |
|-------------------------------|----------------------------------------------|--------------------------------------|
|                               | <span data-ttu-id="ad877-187">**Buffer e trame Simultaneous-Access**</span><span class="sxs-lookup"><span data-stu-id="ad877-187">**Buffers and Simultaneous-Access Textures**</span></span> | <span data-ttu-id="ad877-188">**Trame senza accesso simultaneo**</span><span class="sxs-lookup"><span data-stu-id="ad877-188">**Non-Simultaneous-Access Textures**</span></span> |
| <span data-ttu-id="ad877-189">VERTEX \_ e \_ \_ buffer costante</span><span class="sxs-lookup"><span data-stu-id="ad877-189">VERTEX\_AND\_CONSTANT\_BUFFER</span></span> | <span data-ttu-id="ad877-190">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-190">Yes</span></span>                                          | <span data-ttu-id="ad877-191">No</span><span class="sxs-lookup"><span data-stu-id="ad877-191">No</span></span>                                   |
| <span data-ttu-id="ad877-192">\_buffer indice</span><span class="sxs-lookup"><span data-stu-id="ad877-192">INDEX\_BUFFER</span></span>                 | <span data-ttu-id="ad877-193">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-193">Yes</span></span>                                          | <span data-ttu-id="ad877-194">No</span><span class="sxs-lookup"><span data-stu-id="ad877-194">No</span></span>                                   |
| <span data-ttu-id="ad877-195">destinazione di rendering \_</span><span class="sxs-lookup"><span data-stu-id="ad877-195">RENDER\_TARGET</span></span>                | <span data-ttu-id="ad877-196">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-196">Yes</span></span>                                          | <span data-ttu-id="ad877-197">No</span><span class="sxs-lookup"><span data-stu-id="ad877-197">No</span></span>                                   |
| <span data-ttu-id="ad877-198">accesso non ordinato \_</span><span class="sxs-lookup"><span data-stu-id="ad877-198">UNORDERED\_ACCESS</span></span>             | <span data-ttu-id="ad877-199">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-199">Yes</span></span>                                          | <span data-ttu-id="ad877-200">No</span><span class="sxs-lookup"><span data-stu-id="ad877-200">No</span></span>                                   |
| <span data-ttu-id="ad877-201">scrittura APPROFONDIta \_</span><span class="sxs-lookup"><span data-stu-id="ad877-201">DEPTH\_WRITE</span></span>                  | <span data-ttu-id="ad877-202">No<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="ad877-202">No<sup>\*</sup></span></span>                              | <span data-ttu-id="ad877-203">No</span><span class="sxs-lookup"><span data-stu-id="ad877-203">No</span></span>                                   |
| <span data-ttu-id="ad877-204">lettura APPROFONDIta \_</span><span class="sxs-lookup"><span data-stu-id="ad877-204">DEPTH\_READ</span></span>                   | <span data-ttu-id="ad877-205">No<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="ad877-205">No<sup>\*</sup></span></span>                              | <span data-ttu-id="ad877-206">No</span><span class="sxs-lookup"><span data-stu-id="ad877-206">No</span></span>                                   |
| <span data-ttu-id="ad877-207">\_ \_ risorsa shader non pixel \_</span><span class="sxs-lookup"><span data-stu-id="ad877-207">NON\_PIXEL\_SHADER\_RESOURCE</span></span>  | <span data-ttu-id="ad877-208">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-208">Yes</span></span>                                          | <span data-ttu-id="ad877-209">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-209">Yes</span></span>                                  |
| <span data-ttu-id="ad877-210">\_risorsa pixel shader \_</span><span class="sxs-lookup"><span data-stu-id="ad877-210">PIXEL\_SHADER\_RESOURCE</span></span>       | <span data-ttu-id="ad877-211">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-211">Yes</span></span>                                          | <span data-ttu-id="ad877-212">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-212">Yes</span></span>                                  |
| <span data-ttu-id="ad877-213">FLUSSO in \_ uscita</span><span class="sxs-lookup"><span data-stu-id="ad877-213">STREAM\_OUT</span></span>                   | <span data-ttu-id="ad877-214">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-214">Yes</span></span>                                          | <span data-ttu-id="ad877-215">No</span><span class="sxs-lookup"><span data-stu-id="ad877-215">No</span></span>                                   |
| <span data-ttu-id="ad877-216">argomento indiretto \_</span><span class="sxs-lookup"><span data-stu-id="ad877-216">INDIRECT\_ARGUMENT</span></span>            | <span data-ttu-id="ad877-217">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-217">Yes</span></span>                                          | <span data-ttu-id="ad877-218">No</span><span class="sxs-lookup"><span data-stu-id="ad877-218">No</span></span>                                   |
| <span data-ttu-id="ad877-219">COPIA \_ dest</span><span class="sxs-lookup"><span data-stu-id="ad877-219">COPY\_DEST</span></span>                    | <span data-ttu-id="ad877-220">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-220">Yes</span></span>                                          | <span data-ttu-id="ad877-221">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-221">Yes</span></span>                                  |
| <span data-ttu-id="ad877-222">COPIA \_ origine</span><span class="sxs-lookup"><span data-stu-id="ad877-222">COPY\_SOURCE</span></span>                  | <span data-ttu-id="ad877-223">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-223">Yes</span></span>                                          | <span data-ttu-id="ad877-224">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-224">Yes</span></span>                                  |
| <span data-ttu-id="ad877-225">RISOLvi \_ dest</span><span class="sxs-lookup"><span data-stu-id="ad877-225">RESOLVE\_DEST</span></span>                 | <span data-ttu-id="ad877-226">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-226">Yes</span></span>                                          | <span data-ttu-id="ad877-227">No</span><span class="sxs-lookup"><span data-stu-id="ad877-227">No</span></span>                                   |
| <span data-ttu-id="ad877-228">RISOLvi \_ origine</span><span class="sxs-lookup"><span data-stu-id="ad877-228">RESOLVE\_SOURCE</span></span>               | <span data-ttu-id="ad877-229">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-229">Yes</span></span>                                          | <span data-ttu-id="ad877-230">No</span><span class="sxs-lookup"><span data-stu-id="ad877-230">No</span></span>                                   |
| <span data-ttu-id="ad877-231">PREDICAZIONE</span><span class="sxs-lookup"><span data-stu-id="ad877-231">PREDICATION</span></span>                   | <span data-ttu-id="ad877-232">Sì</span><span class="sxs-lookup"><span data-stu-id="ad877-232">Yes</span></span>                                          | <span data-ttu-id="ad877-233">No</span><span class="sxs-lookup"><span data-stu-id="ad877-233">No</span></span>                                   |



 

<span data-ttu-id="ad877-234"><sup>\*</sup>Le risorse di stencil Depth devono essere trame con accesso non simultaneo e pertanto non possono mai essere innalzate di livello in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="ad877-234"><sup>\*</sup>Depth-stencil resources must be non-simultaneous-access textures and thus can never be implicitly promoted.</span></span>

<span data-ttu-id="ad877-235">Quando si verifica questo accesso, la promozione agisce come una barriera di risorsa implicita.</span><span class="sxs-lookup"><span data-stu-id="ad877-235">When this access occurs the promotion acts like an implicit resource barrier.</span></span> <span data-ttu-id="ad877-236">Per gli accessi successivi, le barriere delle risorse saranno necessarie per modificare lo stato delle risorse, se necessario.</span><span class="sxs-lookup"><span data-stu-id="ad877-236">For subsequent accesses, resource barriers will be required to change the resource state if necessary.</span></span> <span data-ttu-id="ad877-237">Si noti che la promozione da uno stato di lettura promosso a più Stati di lettura è valida, ma questo non è il caso per gli Stati di scrittura.</span><span class="sxs-lookup"><span data-stu-id="ad877-237">Note that promotion from one promoted read state into multiple read state is valid, but this is not the case for write states.</span></span>  
<span data-ttu-id="ad877-238">Se, ad esempio, una risorsa nello stato comune viene promossa alla \_ risorsa pixel shader \_ in una chiamata di progetto, può comunque essere promossa a NON_PIXEL \_ \_ risorsa shader | \_Risorsa pixel shader \_ in un'altra chiamata di progetto.</span><span class="sxs-lookup"><span data-stu-id="ad877-238">For example, if a resource in the common state is promoted to PIXEL\_SHADER\_RESOURCE in a Draw call, it can still be promoted to NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE in another Draw call.</span></span> <span data-ttu-id="ad877-239">Tuttavia, se viene usato in un'operazione di scrittura, ad esempio una destinazione di copia, una barriera di transizione dello stato della risorsa dagli Stati di lettura promossi combinati, qui NON_PIXEL \_ \_ risorsa shader | \_Risorsa pixel shader \_ per la copia di \_ dest è necessaria.</span><span class="sxs-lookup"><span data-stu-id="ad877-239">However, if it is used in a write operation, such as a copy destination, a resource state transition barrier from the combined promoted read states, here NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE, to COPY\_DEST is needed.</span></span>  
<span data-ttu-id="ad877-240">Analogamente, se promosso da comune a copia \_ dest, una barriera è ancora necessaria per eseguire la transizione da copia \_ dest a destinazione di rendering \_ .</span><span class="sxs-lookup"><span data-stu-id="ad877-240">Similarly, if promoted from COMMON to COPY\_DEST, a barrier is still required to transition from COPY\_DEST to RENDER\_TARGET.</span></span>

<span data-ttu-id="ad877-241">Si noti che la promozione dello stato comune è "Free" perché non è necessario che la GPU esegua le attese di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ad877-241">Note that common state promotion is "free" in that there is no need for the GPU to perform any synchronization waits.</span></span> <span data-ttu-id="ad877-242">La promozione rappresenta il fatto che le risorse nello stato comune non devono richiedere un ulteriore rilevamento del lavoro o del driver della GPU per supportare determinati accessi.</span><span class="sxs-lookup"><span data-stu-id="ad877-242">The promotion represents the fact that resources in the COMMON state should not require additional GPU work or driver tracking to support certain accesses.</span></span>

### <a name="state-decay-to-common"></a><span data-ttu-id="ad877-243">Stato decadimento in comune</span><span class="sxs-lookup"><span data-stu-id="ad877-243">State decay to common</span></span>

<span data-ttu-id="ad877-244">Il rovescio della promozione dello stato comune è il decadimento dello \_ stato della risorsa D3D12 \_ \_ comune.</span><span class="sxs-lookup"><span data-stu-id="ad877-244">The flip-side of common state promotion is decay back to D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="ad877-245">Le risorse che soddisfano determinati requisiti vengono considerate senza stato e restituiscono lo stato comune quando la GPU termina l'esecuzione di un'operazione [**oggetti executecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) .</span><span class="sxs-lookup"><span data-stu-id="ad877-245">Resources that meet certain requirements are considered to be stateless and effectively return to the common state when the GPU finishes execution of an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation.</span></span> <span data-ttu-id="ad877-246">Il decadimento non si verifica tra gli elenchi di comandi eseguiti insieme nella stessa chiamata **oggetti executecommandlist** .</span><span class="sxs-lookup"><span data-stu-id="ad877-246">Decay does not occur between command lists executed together in the same **ExecuteCommandLists** call.</span></span>

<span data-ttu-id="ad877-247">Quando un'operazione [**oggetti executecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) viene completata sulla GPU, le risorse seguenti determineranno il decadimento:</span><span class="sxs-lookup"><span data-stu-id="ad877-247">The following resources will decay when an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation is completed on the GPU:</span></span>

-   <span data-ttu-id="ad877-248">Risorse a cui si accede in una coda di copia *o*</span><span class="sxs-lookup"><span data-stu-id="ad877-248">Resources being accessed on a Copy queue, *or*</span></span>
-   <span data-ttu-id="ad877-249">Risorse del buffer per qualsiasi tipo di coda *o*</span><span class="sxs-lookup"><span data-stu-id="ad877-249">Buffer resources on any queue type, *or*</span></span>
-   <span data-ttu-id="ad877-250">Le risorse di trama in qualsiasi tipo di coda con il \_ flag di risorsa D3D12 consentono il set di flag di \_ \_ \_ accesso simultaneo \_ *o*</span><span class="sxs-lookup"><span data-stu-id="ad877-250">Texture resources on any queue type that have the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set, *or*</span></span>
-   <span data-ttu-id="ad877-251">Qualsiasi risorsa innalzata in modo implicito a uno stato di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ad877-251">Any resource implicitly promoted to a read-only state.</span></span>

<span data-ttu-id="ad877-252">Analogamente all'innalzamento di stato comune, il decadimento è gratuito in quanto non è necessaria alcuna sincronizzazione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="ad877-252">Like common state promotion, the decay is free in that no additional synchronization is needed.</span></span> <span data-ttu-id="ad877-253">La combinazione di innalzamento di stato comune e decadimento può aiutare a eliminare molte transizioni [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) non necessarie.</span><span class="sxs-lookup"><span data-stu-id="ad877-253">Combining common state promotion and decay can help to eliminate many unnecessary [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions.</span></span> <span data-ttu-id="ad877-254">In alcuni casi, questo può offrire miglioramenti significativi delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ad877-254">In some cases, this can provide significant performance improvements.</span></span>

<span data-ttu-id="ad877-255">I buffer e le risorse di Simultaneous-Access decadono nello stato comune indipendentemente dal fatto che siano stati esplicitamente sottoposti a transizione usando barriere delle risorse o innalzate in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="ad877-255">Buffers and Simultaneous-Access resources will decay to the common state regardless of whether they were explicitly transitioned using resource barriers or implicitly promoted.</span></span>

### <a name="performance-implications"></a><span data-ttu-id="ad877-256">Implicazioni per le prestazioni</span><span class="sxs-lookup"><span data-stu-id="ad877-256">Performance implications</span></span>

<span data-ttu-id="ad877-257">Quando si registrano transizioni [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) esplicite nelle risorse nello stato comune, è corretto usare lo stato \_ della risorsa D3D12 \_ \_ comune o qualsiasi stato promuovibile come valore di *rimboschimento* nella struttura della \_ barriera della transizione di risorse D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ad877-257">When recording explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions on resources in the common state, it is correct to use either D3D12\_RESOURCE\_STATE\_COMMON or any promotable state as the *BeforeState* value in the D3D12\_RESOURCE\_TRANSITION\_BARRIER structure.</span></span> <span data-ttu-id="ad877-258">Questo consente la gestione dello stato tradizionale che ignora il decadimento automatico dei buffer e delle trame ad accesso simultaneo.</span><span class="sxs-lookup"><span data-stu-id="ad877-258">This allows traditional state management that ignores automatic decay of buffers and simultaneous-access textures.</span></span> <span data-ttu-id="ad877-259">Questo potrebbe non essere auspicabile, in quanto evitando che le chiamate **ResourceBarrier** di transizione con risorse note nello stato comune possano migliorare significativamente le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ad877-259">This may not be desirable though, as avoiding transition **ResourceBarrier** calls with resources known to be in the common state can significantly improve performance.</span></span> <span data-ttu-id="ad877-260">Le barriere alle risorse possono essere costose.</span><span class="sxs-lookup"><span data-stu-id="ad877-260">Resource barriers can be expensive.</span></span> <span data-ttu-id="ad877-261">Sono progettati per forzare gli scaricamenti della cache, le modifiche al layout di memoria e altre sincronizzazioni che potrebbero non essere necessarie per le risorse già nello stato comune.</span><span class="sxs-lookup"><span data-stu-id="ad877-261">They are designed to force cache flushes, memory layout changes and other synchronization that may not be necessary for resources already in the common state.</span></span> <span data-ttu-id="ad877-262">Un elenco di comandi che usa una barriera delle risorse da uno stato non comune a un altro stato non comune in una risorsa attualmente nello stato comune può presentare un sovraccarico non necessario.</span><span class="sxs-lookup"><span data-stu-id="ad877-262">A command list that uses a resource barrier from a non-common state to another non-common state on a resource currently in the common state can introduce a lot of unneeded overhead.</span></span>

<span data-ttu-id="ad877-263">Evitare inoltre transizioni esplicite di [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) per \_ lo stato della risorsa D3D12, a \_ \_ meno che non sia assolutamente necessario (ad esempio, l'accesso successivo si trova in una coda dei comandi di copia che richiede che le risorse inizino nello stato comune).</span><span class="sxs-lookup"><span data-stu-id="ad877-263">Also, avoid explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions to D3D12\_RESOURCE\_STATE\_COMMON unless absolutely necessary (e.g. the next access is on a COPY command queue which requires a resources begin in the common state).</span></span> <span data-ttu-id="ad877-264">Una transizione eccessiva allo stato comune può rallentare notevolmente le prestazioni della GPU.</span><span class="sxs-lookup"><span data-stu-id="ad877-264">Excessive transitions to the common state can dramatically slow down GPU performance.</span></span>

<span data-ttu-id="ad877-265">In sintesi, provare a basarsi sull'innalzamento di stato comune e il decadimento ogni volta che la semantica consente di uscire senza emettere chiamate [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) .</span><span class="sxs-lookup"><span data-stu-id="ad877-265">In summary, try to rely on common state promotion and decay whenever its semantics let you get away without issuing [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) calls.</span></span>

## <a name="split-barriers"></a><span data-ttu-id="ad877-266">Suddividere le barriere</span><span class="sxs-lookup"><span data-stu-id="ad877-266">Split Barriers</span></span>

<span data-ttu-id="ad877-267">Una barriera di transizione delle risorse con il flag di blocco della \_ barriera delle risorse D3D12 \_ \_ \_ \_ inizia una barriera divisa e la barriera di transizione è detta in sospeso.</span><span class="sxs-lookup"><span data-stu-id="ad877-267">A resource transition barrier with the D3D12\_RESOURCE\_BARRIER\_FLAG\_BEGIN\_ONLY flag begins a split barrier and the transition barrier is said to be pending.</span></span> <span data-ttu-id="ad877-268">Mentre la barriera è in sospeso, la risorsa (Sub) non può essere letta o scritta dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="ad877-268">While the barrier is pending the (sub)resource cannot be read or written by the GPU.</span></span> <span data-ttu-id="ad877-269">L'unica barriera di transizione legale che può essere applicata a una risorsa (Sub) con una barriera in sospeso è uno con gli stessi stati *before* e *after* e il \_ flag di fine del flag di barriera della risorsa D3D12, la \_ \_ \_ \_ cui barriera completa la transizione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="ad877-269">The only legal transition barrier that can be applied to a (sub)resource with a pending barrier is one with the same *before* and *after* states and the D3D12\_RESOURCE\_BARRIER\_FLAG\_END\_ONLY flag, which barrier completes the pending transition.</span></span>

<span data-ttu-id="ad877-270">Le barriere Split forniscono suggerimenti alla GPU che una risorsa nello stato a verrà successivamente usata nello stato *B* in *un* secondo momento.</span><span class="sxs-lookup"><span data-stu-id="ad877-270">Split barriers provide hints to the GPU that a resource in state *A* will next be used in state *B* sometime later.</span></span> <span data-ttu-id="ad877-271">In questo modo l'opzione GPU consente di ottimizzare il carico di lavoro di transizione, possibilmente riducendo o eliminando i blocchi di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ad877-271">This gives the GPU the option to optimize the transition workload, possibly reducing or eliminating execution stalls.</span></span> <span data-ttu-id="ad877-272">Il rilascio della barriera di sola fine garantisce che tutte le operazioni di transizione GPU siano finite prima di passare al comando successivo.</span><span class="sxs-lookup"><span data-stu-id="ad877-272">Issuing the end-only barrier guarantees that all GPU transition work is finished before moving onto the next command.</span></span>

<span data-ttu-id="ad877-273">L'uso di barriere Split può contribuire a migliorare le prestazioni, soprattutto in scenari con più motori o in cui le risorse sono in lettura/scrittura in modo sparse in uno o più elenchi di comandi.</span><span class="sxs-lookup"><span data-stu-id="ad877-273">Using split barriers can help to improve performance, especially in multi-engine scenarios or where resources are read/write transitioned sparsely throughout one or more command lists.</span></span>

## <a name="resource-barrier-example-scenario"></a><span data-ttu-id="ad877-274">Scenario di esempio di barriera delle risorse</span><span class="sxs-lookup"><span data-stu-id="ad877-274">Resource barrier example scenario</span></span>

<span data-ttu-id="ad877-275">Nei frammenti di codice seguenti viene illustrato l'utilizzo del metodo [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) in un esempio multithread.</span><span class="sxs-lookup"><span data-stu-id="ad877-275">The following snippets show the use of the [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) method in a multi-threading sample.</span></span>

<span data-ttu-id="ad877-276">Creazione della visualizzazione depth stencil, transizione a uno stato scrivibile.</span><span class="sxs-lookup"><span data-stu-id="ad877-276">Creating the depth stencil view, transitioning it to a writeable state.</span></span>


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



<span data-ttu-id="ad877-277">Creazione della visualizzazione buffer dei vertici, prima modifica da uno stato comune a una destinazione, quindi da una destinazione a uno stato leggibile generico.</span><span class="sxs-lookup"><span data-stu-id="ad877-277">Creating the vertex buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


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



<span data-ttu-id="ad877-278">Creazione della visualizzazione buffer dell'indice, prima modifica da uno stato comune a una destinazione, quindi da una destinazione a uno stato leggibile generico.</span><span class="sxs-lookup"><span data-stu-id="ad877-278">Creating the index buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


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



<span data-ttu-id="ad877-279">Creazione di trame e visualizzazioni delle risorse dello shader.</span><span class="sxs-lookup"><span data-stu-id="ad877-279">Creating textures and shader resource views.</span></span> <span data-ttu-id="ad877-280">La trama viene modificata da uno stato comune a una destinazione e quindi da una destinazione a una risorsa pixel shader.</span><span class="sxs-lookup"><span data-stu-id="ad877-280">The texture is changed from a common state to a destination, and then from a destination to a pixel shader resource.</span></span>


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



<span data-ttu-id="ad877-281">Inizio di un frame; Questa operazione non solo utilizza [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) per indicare che il backBuffer deve essere utilizzato come destinazione di rendering, ma inizializza anche la risorsa frame, che chiama **ResourceBarrier** sul buffer depth stencil.</span><span class="sxs-lookup"><span data-stu-id="ad877-281">Beginning a frame; this not only uses [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to indicate that the backbuffer is to be used as a render target, but also initializes the frame resource (which calls **ResourceBarrier** on the depth stencil buffer).</span></span>


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



<span data-ttu-id="ad877-282">Terminazione di un frame, che indica che il buffer nascosto è ora usato per presentare.</span><span class="sxs-lookup"><span data-stu-id="ad877-282">Ending a frame, indicating the back buffer is now used to present.</span></span>


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



<span data-ttu-id="ad877-283">L'inizializzazione di una risorsa frame, chiamata quando si inizia un frame, esegue la transizione del buffer di depth stencil a scrivibile.</span><span class="sxs-lookup"><span data-stu-id="ad877-283">Initializing a frame resource, called when beginning a frame, transitions the depth stencil buffer to writeable.</span></span>


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



<span data-ttu-id="ad877-284">Le barriere sono invertite a metà Frame e la transizione della mappa Shadow da scrivibile a leggibile.</span><span class="sxs-lookup"><span data-stu-id="ad877-284">Barriers are swapped mid-frame, transitioning the shadow map from writeable to readable.</span></span>


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



<span data-ttu-id="ad877-285">Finish viene chiamato quando viene terminato un frame, passando il mapping dell'ombreggiatura a uno stato comune.</span><span class="sxs-lookup"><span data-stu-id="ad877-285">Finish is called when a frame is ended, transitioning the shadow map to a common state.</span></span>


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a><span data-ttu-id="ad877-286">Esempio di promozione e decadimento dello stato comune</span><span class="sxs-lookup"><span data-stu-id="ad877-286">Common state promotion and decay sample</span></span>

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

## <a name="example-of-split-barriers"></a><span data-ttu-id="ad877-287">Esempio di barriere Split</span><span class="sxs-lookup"><span data-stu-id="ad877-287">Example of split barriers</span></span>

<span data-ttu-id="ad877-288">Nell'esempio seguente viene illustrato come utilizzare una barriera Split per ridurre le stallo della pipeline.</span><span class="sxs-lookup"><span data-stu-id="ad877-288">The following example shows how to use a split barrier to reduce pipeline stalls.</span></span> <span data-ttu-id="ad877-289">Il codice che segue non usa le barriere Split:</span><span class="sxs-lookup"><span data-stu-id="ad877-289">The code that follows does not use split barriers:</span></span>

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

<span data-ttu-id="ad877-290">Il codice seguente usa le barriere Split:</span><span class="sxs-lookup"><span data-stu-id="ad877-290">The following code uses split barriers:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ad877-291">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad877-291">Related topics</span></span>

[<span data-ttu-id="ad877-292">Esercitazioni video su DirectX Advanced Learning: barriere delle risorse e rilevamento dello stato</span><span class="sxs-lookup"><span data-stu-id="ad877-292">DirectX advanced learning video tutorials : Resource Barriers and State Tracking</span></span>](https://www.youtube.com/watch?v=nmB2XMasz2o)

[<span data-ttu-id="ad877-293">Sincronizzazione multimotore</span><span class="sxs-lookup"><span data-stu-id="ad877-293">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)

[<span data-ttu-id="ad877-294">Invio di lavoro in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="ad877-294">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)

[<span data-ttu-id="ad877-295">Uno sguardo all'interno delle barriere dello stato della risorsa D3D12</span><span class="sxs-lookup"><span data-stu-id="ad877-295">A Look Inside D3D12 Resource State Barriers</span></span>](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

