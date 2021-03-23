---
title: Predicazione
description: Predicazione è una funzionalità che consente alla GPU anziché alla CPU di determinare di non creare, copiare o inviare un oggetto.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/20/2020
ms.locfileid: "104548869"
---
# <a name="predication"></a><span data-ttu-id="601dd-103">Predicazione</span><span class="sxs-lookup"><span data-stu-id="601dd-103">Predication</span></span>

<span data-ttu-id="601dd-104">Predicazione è una funzionalità che consente alla GPU anziché alla CPU di determinare di non creare, copiare o inviare un oggetto.</span><span class="sxs-lookup"><span data-stu-id="601dd-104">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy, or dispatch an object.</span></span>

-   [<span data-ttu-id="601dd-105">Overview</span><span class="sxs-lookup"><span data-stu-id="601dd-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="601dd-106">SetPredication</span><span class="sxs-lookup"><span data-stu-id="601dd-106">SetPredication</span></span>](#setpredication)
-   [<span data-ttu-id="601dd-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="601dd-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="601dd-108">Panoramica</span><span class="sxs-lookup"><span data-stu-id="601dd-108">Overview</span></span>

<span data-ttu-id="601dd-109">L'uso tipico di predicazione è con occlusione; Se viene disegnato un rettangolo di delimitazione, non esiste ovviamente alcun punto per disegnare l'oggetto stesso.</span><span class="sxs-lookup"><span data-stu-id="601dd-109">The typical use of predication is with occlusion; if a bounding box is drawn and is occluded, there is obviously no point in drawing the object itself.</span></span> <span data-ttu-id="601dd-110">In questa situazione, il disegno dell'oggetto può essere "predicato", consentendo la rimozione dal rendering effettivo da parte della GPU.</span><span class="sxs-lookup"><span data-stu-id="601dd-110">In this situation, the drawing of the object can be "predicated", enabling its removal from actual rendering by the GPU.</span></span>

<span data-ttu-id="601dd-111">Inizialmente, questo potrebbe sembrare redudant oltre il test di profondità standard più un passaggio di profondità iniziale.</span><span class="sxs-lookup"><span data-stu-id="601dd-111">At first, this might seem redudant over and above the standard depth test plus an early depth pass.</span></span> <span data-ttu-id="601dd-112">Tuttavia, predicazione può rimuovere l'overhead dello stato del comando di disegna, più la rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="601dd-112">But predication can remove the overhead of the draw command state itself, plus the rasterization.</span></span> <span data-ttu-id="601dd-113">Mentre un passaggio di profondità iniziale rimuove i pixel superflui, può comunque eseguire gli shader vertex, Hull, Domain e Geometry e richiamare l'assembler di input della funzione fissa, Tesselator e rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="601dd-113">While an early depth pass removes unnecessary pixels, it can still execute vertex, hull, domain, and geometry shaders, and invoke the fixed-function input assembler, tesselator, and rasterizer.</span></span> <span data-ttu-id="601dd-114">Disegnando un semplice rettangolo di delimitazione o un volume di delimitazione simile &mdash; , più semplice da elaborare e rasterizzare rispetto al modello reale, &mdash; si evita la rasterizzazione e l'elaborazione superflue.</span><span class="sxs-lookup"><span data-stu-id="601dd-114">By drawing a simple bounding box or similar bounding volume&mdash;which is simpler to process and rasterize than the real model&mdash;you avoid unnecessary rasterization and processing.</span></span>

<span data-ttu-id="601dd-115">A differenza di Direct3D 11, predicazione è separato dalle query ed è espanso in Direct3D 12 per consentire a un'applicazione di predicare gli oggetti in base a qualsiasi motivo per cui lo sviluppatore dell'app può decidere (non solo occlusione).</span><span class="sxs-lookup"><span data-stu-id="601dd-115">Unlike Direct3D 11, predication is decoupled from queries, and is expanded in Direct3D 12 to enable an application to predicate objects based on any reasoning the app developer may decide on (not just occlusion).</span></span>

## <a name="setpredication"></a><span data-ttu-id="601dd-116">SetPredication</span><span class="sxs-lookup"><span data-stu-id="601dd-116">SetPredication</span></span>

<span data-ttu-id="601dd-117">Predicazione può essere impostato in base al valore di 64 bit all'interno di un buffer (vedere [**D3D12 \_ predicazione \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).</span><span class="sxs-lookup"><span data-stu-id="601dd-117">Predication can be set based on the value of 64-bits within a buffer (refer to [**D3D12\_PREDICATION\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).</span></span>

<span data-ttu-id="601dd-118">Quando la GPU esegue un comando [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) , blocca il valore nel buffer.</span><span class="sxs-lookup"><span data-stu-id="601dd-118">When the GPU executes a [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) command it snaps the value in the buffer.</span></span> <span data-ttu-id="601dd-119">Le modifiche future apportate ai dati nel buffer non influiscono in modo retroattivo sullo stato predicazione.</span><span class="sxs-lookup"><span data-stu-id="601dd-119">Future changes to the data in the buffer do not retroactively affect the predication state.</span></span>

<span data-ttu-id="601dd-120">Se il buffer del parametro di input è NULL, predicazione è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="601dd-120">If the input parameter Buffer is NULL, then predication is disabled.</span></span>

<span data-ttu-id="601dd-121">Gli hint predicazione non sono presenti nell'API Direct3D 12. e predicazione sono consentiti negli elenchi di comandi Direct, COMPUTE e Copy.</span><span class="sxs-lookup"><span data-stu-id="601dd-121">Predication hints are not present in the Direct3D 12 API; and predication is allowed on direct, compute, and copy command lists.</span></span> <span data-ttu-id="601dd-122">Il buffer di origine può trovarsi in qualsiasi tipo di heap (impostazione predefinita, caricamento, readback, personalizzata).</span><span class="sxs-lookup"><span data-stu-id="601dd-122">The source buffer can be in any heap type (default, upload, readback, custom).</span></span>

<span data-ttu-id="601dd-123">Il runtime di base convaliderà quanto segue:</span><span class="sxs-lookup"><span data-stu-id="601dd-123">The core runtime will validate the following:</span></span>

-   <span data-ttu-id="601dd-124">*AlignedBufferOffset* è un multiplo di 8 byte</span><span class="sxs-lookup"><span data-stu-id="601dd-124">*AlignedBufferOffset* is a multiple of 8 bytes</span></span>
-   <span data-ttu-id="601dd-125">La risorsa è un buffer</span><span class="sxs-lookup"><span data-stu-id="601dd-125">The resource is a buffer</span></span>
-   <span data-ttu-id="601dd-126">L'operazione è un membro valido dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="601dd-126">The operation is a valid member of the enumeration</span></span>
-   <span data-ttu-id="601dd-127">Non è possibile chiamare [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) dall'interno di un bundle</span><span class="sxs-lookup"><span data-stu-id="601dd-127">[**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) cannot be called from within a bundle</span></span>
-   <span data-ttu-id="601dd-128">Il tipo di elenco dei comandi supporta predicazione</span><span class="sxs-lookup"><span data-stu-id="601dd-128">The command list type supports predication</span></span>
-   <span data-ttu-id="601dd-129">L'offset non supera la dimensione del buffer</span><span class="sxs-lookup"><span data-stu-id="601dd-129">The offset does not exceed the buffer size</span></span>

<span data-ttu-id="601dd-130">Il livello di debug genererà un errore se il buffer di origine non si trova nel [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (che corrisponde allo stato [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)e semplicemente a un alias).</span><span class="sxs-lookup"><span data-stu-id="601dd-130">The debug layer will issue an error if the source buffer is not in the [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (which is the same as [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states), and simply an alias) state.</span></span>

<span data-ttu-id="601dd-131">Il set di operazioni che è possibile predicare è il seguente:</span><span class="sxs-lookup"><span data-stu-id="601dd-131">The set of operations which can be predicated are:</span></span>

-   [<span data-ttu-id="601dd-132">**DrawInstanced**</span><span class="sxs-lookup"><span data-stu-id="601dd-132">**DrawInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [<span data-ttu-id="601dd-133">**DrawIndexedInstanced**</span><span class="sxs-lookup"><span data-stu-id="601dd-133">**DrawIndexedInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [<span data-ttu-id="601dd-134">**Dispatch**</span><span class="sxs-lookup"><span data-stu-id="601dd-134">**Dispatch**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="601dd-135">**CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="601dd-135">**CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="601dd-136">**CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="601dd-136">**CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="601dd-137">**CopyResource**</span><span class="sxs-lookup"><span data-stu-id="601dd-137">**CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="601dd-138">**CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="601dd-138">**CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="601dd-139">**ResolveSubresource**</span><span class="sxs-lookup"><span data-stu-id="601dd-139">**ResolveSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [<span data-ttu-id="601dd-140">**ClearDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="601dd-140">**ClearDepthStencilView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [<span data-ttu-id="601dd-141">**ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="601dd-141">**ClearRenderTargetView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [<span data-ttu-id="601dd-142">**ClearUnorderedAccessViewUint**</span><span class="sxs-lookup"><span data-stu-id="601dd-142">**ClearUnorderedAccessViewUint**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="601dd-143">**ClearUnorderedAccessViewFloat**</span><span class="sxs-lookup"><span data-stu-id="601dd-143">**ClearUnorderedAccessViewFloat**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="601dd-144">**ExecuteIndirect**</span><span class="sxs-lookup"><span data-stu-id="601dd-144">**ExecuteIndirect**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

<span data-ttu-id="601dd-145">[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) non è predicato.</span><span class="sxs-lookup"><span data-stu-id="601dd-145">[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) is not predicated itself.</span></span> <span data-ttu-id="601dd-146">Al contrario, vengono predicate le singole operazioni dall'elenco precedente che sono contenute in parte del bundle.</span><span class="sxs-lookup"><span data-stu-id="601dd-146">Instead, individual operations from the list above which are contained in side of the bundle are predicated.</span></span>

<span data-ttu-id="601dd-147">I metodi ID3D12GraphicsCommandList [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) non sono predicati.</span><span class="sxs-lookup"><span data-stu-id="601dd-147">The ID3D12GraphicsCommandList methods [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) and [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) are not predicated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="601dd-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="601dd-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="601dd-149">Contatori e query</span><span class="sxs-lookup"><span data-stu-id="601dd-149">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="601dd-150">Misurazione delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="601dd-150">Performance Measurement</span></span>](performance-measurement.md)
</dt> <dt>

[<span data-ttu-id="601dd-151">Procedura dettagliata per le query predicazione</span><span class="sxs-lookup"><span data-stu-id="601dd-151">Predication queries walk-through</span></span>](predication-queries.md)
</dt> </dl>

 

 




