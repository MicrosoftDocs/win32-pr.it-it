---
title: Contatori UAV
description: È possibile usare i contatori di Access-View (UAV) non ordinati per associare un contatore atomico a 32 bit a una visualizzazione non ordinata (UAV).
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: 94bc1492e3b984d96c76788430d2e63c0672ca76
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104548817"
---
# <a name="uav-counters"></a><span data-ttu-id="e5f7e-103">Contatori UAV</span><span class="sxs-lookup"><span data-stu-id="e5f7e-103">UAV Counters</span></span>
<span data-ttu-id="e5f7e-104">È possibile usare i contatori di Access-View (UAV) non ordinati per associare un contatore atomico a 32 bit a una visualizzazione non ordinata (UAV).</span><span class="sxs-lookup"><span data-stu-id="e5f7e-104">You can use unordered-access-view (UAV) counters to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span>

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="e5f7e-105">Differenze nei contatori UAV da Direct3D 11 a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e5f7e-105">Differences in UAV counters from Direct3D 11 to Direct3D 12</span></span>
<span data-ttu-id="e5f7e-106">Le app Direct3D 12 e Direct3D 11 usano entrambe le stesse funzioni shader HLSL (High-Level Shader Language) per accedere ai contatori UAV.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-106">Direct3D 12 apps and Direct3D 11 apps both use the same high-level shader language (HLSL) shader functions to access the UAV counters.</span></span>

-   <span data-ttu-id="e5f7e-107">**IncrementCounter**</span><span class="sxs-lookup"><span data-stu-id="e5f7e-107">**IncrementCounter**</span></span>
-   <span data-ttu-id="e5f7e-108">**DecrementCounter**</span><span class="sxs-lookup"><span data-stu-id="e5f7e-108">**DecrementCounter**</span></span>
-   <span data-ttu-id="e5f7e-109">**Accoda**</span><span class="sxs-lookup"><span data-stu-id="e5f7e-109">**Append**</span></span>
-   <span data-ttu-id="e5f7e-110">**Utilizzo**</span><span class="sxs-lookup"><span data-stu-id="e5f7e-110">**Consume**</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="e5f7e-111">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e5f7e-111">Direct3D 12</span></span>
<span data-ttu-id="e5f7e-112">In Direct3D 12, i valori a 32 bit vengono allocati dall'applicazione, quindi i valori a 32 bit possono essere letti e scritti dalla CPU o dalla GPU, esattamente come qualsiasi altra risorsa Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-112">In Direct3D 12, the 32-bit values are allocated by the application, so the 32-bit values can be read and written by either the CPU or the GPU, just like any other Direct3D 12 resource.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="e5f7e-113">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e5f7e-113">Direct3D 11</span></span>
<span data-ttu-id="e5f7e-114">Al di fuori degli shader, con Direct3D 11 è necessario chiamare i metodi API per accedere ai contatori (ad esempio, [sul ID3D11DeviceContext:: CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).</span><span class="sxs-lookup"><span data-stu-id="e5f7e-114">Outside of the shaders, with Direct3D 11 you need to call API methods in order to access the counters (for example, [ID3D11DeviceContext::CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).</span></span>

## <a name="using-uav-counters"></a><span data-ttu-id="e5f7e-115">Uso dei contatori UAV</span><span class="sxs-lookup"><span data-stu-id="e5f7e-115">Using UAV counters</span></span>
<span data-ttu-id="e5f7e-116">L'app è responsabile dell'allocazione di 32 bit di archiviazione per i contatori UAV.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-116">Your app is responsible for allocating 32-bits of storage for UAV counters.</span></span> <span data-ttu-id="e5f7e-117">Questo spazio di archiviazione può essere allocato in una risorsa diversa da quella che contiene i dati accessibili tramite il UAV.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-117">This storage can be allocated in a different resource as the one that contains data accessible via the UAV.</span></span>

<span data-ttu-id="e5f7e-118">Vedere [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12 \_ buffer \_ UAV \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) e [**D3D12 \_ buffer \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).</span><span class="sxs-lookup"><span data-stu-id="e5f7e-118">Refer to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12\_BUFFER\_UAV\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) and [**D3D12\_BUFFER\_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).</span></span>

<span data-ttu-id="e5f7e-119">Se nella chiamata a [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)è specificato *pCounterResource* , è presente un contatore associato a UAV.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-119">If *pCounterResource* is specified in the call to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), then there is a counter associated with the UAV.</span></span> <span data-ttu-id="e5f7e-120">In questo caso:</span><span class="sxs-lookup"><span data-stu-id="e5f7e-120">In this case:</span></span>

-   <span data-ttu-id="e5f7e-121">*StructureByteStride* deve essere maggiore di zero</span><span class="sxs-lookup"><span data-stu-id="e5f7e-121">*StructureByteStride* must be greater than zero</span></span>
-   <span data-ttu-id="e5f7e-122">Il formato del formato deve essere DXGI \_ \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="e5f7e-122">Format must be DXGI\_FORMAT\_UNKNOWN</span></span>
-   <span data-ttu-id="e5f7e-123">Non è necessario impostare il flag RAW</span><span class="sxs-lookup"><span data-stu-id="e5f7e-123">The RAW flag must not be set</span></span>
-   <span data-ttu-id="e5f7e-124">Entrambe le risorse devono essere buffer</span><span class="sxs-lookup"><span data-stu-id="e5f7e-124">Both of the resources must be buffers</span></span>
-   <span data-ttu-id="e5f7e-125">*CounterOffsetInBytes* deve essere un multiplo di 4 byte</span><span class="sxs-lookup"><span data-stu-id="e5f7e-125">*CounterOffsetInBytes* must be a multiple of 4 bytes</span></span>
-   <span data-ttu-id="e5f7e-126">*CounterOffsetInBytes* deve essere compreso nell'intervallo della risorsa contatore</span><span class="sxs-lookup"><span data-stu-id="e5f7e-126">*CounterOffsetInBytes* must be within the range of the counter resource</span></span>
-   <span data-ttu-id="e5f7e-127">*pDesc* non può essere null</span><span class="sxs-lookup"><span data-stu-id="e5f7e-127">*pDesc* cannot be NULL</span></span>
-   <span data-ttu-id="e5f7e-128">la *preorigine* non può essere null</span><span class="sxs-lookup"><span data-stu-id="e5f7e-128">*pResource* cannot be NULL</span></span>

<span data-ttu-id="e5f7e-129">E si notino i casi d'uso seguenti:</span><span class="sxs-lookup"><span data-stu-id="e5f7e-129">And note the following use cases:</span></span>

-   <span data-ttu-id="e5f7e-130">Se *pCounterResource* non è specificato, *CounterOffsetInBytes* deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-130">If *pCounterResource* is not specified, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="e5f7e-131">Se viene impostato il flag RAW, il formato deve essere DXGI \_ Format \_ R32 senza \_ tipo e la risorsa UAV deve essere un buffer.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-131">If the RAW flag is set then the format must be DXGI\_FORMAT\_R32\_TYPELESS and the UAV resource must be a buffer.</span></span>
-   <span data-ttu-id="e5f7e-132">Se *pCounterResource* non è impostato, *CounterOffsetInBytes* deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-132">If *pCounterResource* is not set, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="e5f7e-133">Se il flag RAW non è impostato e *StructureByteStride* = 0, il formato deve essere un formato UAV valido.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-133">If the RAW flag is not set and *StructureByteStride* = 0, then the format must be a valid UAV format.</span></span>

<span data-ttu-id="e5f7e-134">Direct3D 12 rimuove la distinzione tra Append e Counter UAV (anche se la distinzione esiste ancora nel bytecode HLSL).</span><span class="sxs-lookup"><span data-stu-id="e5f7e-134">Direct3D 12 removes the distinction between append and counter UAVs (although the distinction still exists in HLSL bytecode).</span></span>

<span data-ttu-id="e5f7e-135">Il runtime di base convaliderà queste restrizioni all'interno di [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span><span class="sxs-lookup"><span data-stu-id="e5f7e-135">The core runtime will validate these restrictions inside of [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span></span>

<span data-ttu-id="e5f7e-136">Durante il progetto o la distribuzione, la risorsa contatore deve trovarsi nello stato della [**\_ risorsa D3D12 \_ \_ \_ accesso non ordinato**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).</span><span class="sxs-lookup"><span data-stu-id="e5f7e-136">During Draw/Dispatch, the counter resource must be in the state [**D3D12\_RESOURCE\_STATE\_UNORDERED\_ACCESS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).</span></span> <span data-ttu-id="e5f7e-137">Inoltre, all'interno di una singola chiamata di estrazione/invio, non è valido per un'applicazione accedere alla stessa posizione di memoria a 32 bit tramite due contatori UAV distinti.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-137">Also, within a single Draw/Dispatch call, it is invalid for an application to access the same 32-bit memory location via two separate UAV counters.</span></span> <span data-ttu-id="e5f7e-138">Il livello di debug emetterà errori se viene rilevata una di queste.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-138">The debug layer will issue errors if either of these is detected.</span></span>

<span data-ttu-id="e5f7e-139">Non sono disponibili metodi "SetUnorderedAccessViewCounterValue" o "CopyStructureCount" perché le app possono semplicemente copiare i dati direttamente da e verso il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-139">There are no "SetUnorderedAccessViewCounterValue" or "CopyStructureCount" methods because apps can simply copy data to and from the counter value directly.</span></span>

<span data-ttu-id="e5f7e-140">L'indicizzazione dinamica di UAV con contatori è supportata.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-140">Dynamic indexing of UAVs with counters is supported.</span></span>

<span data-ttu-id="e5f7e-141">Se uno shader tenta di accedere al contatore di un UAV a cui non è associato alcun contatore, il livello di debug emetterà un avviso e si verificherà un errore di pagina GPU causando la rimozione del dispositivo dell'app.</span><span class="sxs-lookup"><span data-stu-id="e5f7e-141">If a shader attempts to access the counter of a UAV that does not have an associated counter, then the debug layer will issue a warning, and a GPU page fault will occur causing the apps’s device to be removed.</span></span>

<span data-ttu-id="e5f7e-142">I contatori UAV sono supportati in tutti i tipi di heap (impostazione predefinita, upload, readback).</span><span class="sxs-lookup"><span data-stu-id="e5f7e-142">UAV counters are supported in all heap types (default, upload, readback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5f7e-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5f7e-143">Related topics</span></span>

* [<span data-ttu-id="e5f7e-144">Contatori e query</span><span class="sxs-lookup"><span data-stu-id="e5f7e-144">Counters and queries</span></span>](counters-and-queries.md)