---
title: Caricamento di dati di trama tramite buffer
description: Il caricamento di dati di trama 2D o 3D è simile al caricamento di dati 1D, ad eccezione del fatto che le applicazioni devono prestare maggiore attenzione all'allineamento dei dati correlati all'altezza delle righe.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72177be1fefbf102e901d28d47413c8bcff41ab
ms.sourcegitcommit: 39754f1af7853adff2525d0936afe9aad2066a9a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/22/2021
ms.locfileid: "112426965"
---
# <a name="uploading-texture-data-through-buffers"></a><span data-ttu-id="5df95-103">Caricamento di dati di trama tramite buffer</span><span class="sxs-lookup"><span data-stu-id="5df95-103">Uploading Texture Data Through Buffers</span></span>

<span data-ttu-id="5df95-104">Il caricamento di dati di trama 2D o 3D è simile al caricamento di dati 1D, ad eccezione del fatto che le applicazioni devono prestare maggiore attenzione all'allineamento dei dati correlati all'altezza delle righe.</span><span class="sxs-lookup"><span data-stu-id="5df95-104">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="5df95-105">I buffer possono essere usati in modo ortogonale e simultaneo da più parti della pipeline grafica e sono molto flessibili.</span><span class="sxs-lookup"><span data-stu-id="5df95-105">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span>

-   [<span data-ttu-id="5df95-106">Caricare dati di trama tramite buffer</span><span class="sxs-lookup"><span data-stu-id="5df95-106">Upload Texture Data via Buffers</span></span>](#upload-texture-data-via-buffers)
-   [<span data-ttu-id="5df95-107">Copia</span><span class="sxs-lookup"><span data-stu-id="5df95-107">Copying</span></span>](#copying)
-   [<span data-ttu-id="5df95-108">Mapping e annullamento del mapping</span><span class="sxs-lookup"><span data-stu-id="5df95-108">Mapping and unmapping</span></span>](#mapping-and-unmapping)
-   [<span data-ttu-id="5df95-109">Allineamento del buffer</span><span class="sxs-lookup"><span data-stu-id="5df95-109">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="5df95-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5df95-110">Related topics</span></span>](#related-topics)

## <a name="upload-texture-data-via-buffers"></a><span data-ttu-id="5df95-111">Caricare dati di trama tramite buffer</span><span class="sxs-lookup"><span data-stu-id="5df95-111">Upload Texture Data via Buffers</span></span>

<span data-ttu-id="5df95-112">Le applicazioni devono caricare i dati [**tramite ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) [**o ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion).</span><span class="sxs-lookup"><span data-stu-id="5df95-112">Applications must upload data via [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion).</span></span> <span data-ttu-id="5df95-113">È molto più probabile che i dati di trama siano più grandi, a cui si accede ripetutamente e traggono vantaggio dalla coesistenza della cache migliorata dei layout di memoria non lineare rispetto ad altri dati delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5df95-113">Texture data is much more likely to be larger, accessed repeatedly, and benefit from the improved cache-coherency of non-linear memory layouts than other resource data.</span></span> <span data-ttu-id="5df95-114">Quando i buffer vengono usati in D3D12, le applicazioni hanno il controllo completo sul posizionamento e sulla disposizione dei dati associati alla copia dei dati delle risorse, purché siano soddisfatti i requisiti di allineamento della memoria.</span><span class="sxs-lookup"><span data-stu-id="5df95-114">When buffers are used in D3D12, applications have full control on data placement and arrangement associated with copying resource data around, as long as the memory alignment requirements are satisfied.</span></span>

<span data-ttu-id="5df95-115">L'esempio evidenzia dove l'applicazione appiatti semplicemente i dati 2D in 1D prima di posizionarlo nel buffer.</span><span class="sxs-lookup"><span data-stu-id="5df95-115">The sample highlights where the application simply flattens 2D data into 1D before placing it in the buffer.</span></span> <span data-ttu-id="5df95-116">Per lo scenario mipmap 2D, l'applicazione può appiattire ogni sotto-risorsa in modo discreto e usare rapidamente un algoritmo di sottoallocazione 1D oppure usare una tecnica di sottoallocazione 2D più complessa per ridurre al minimo l'utilizzo della memoria video.</span><span class="sxs-lookup"><span data-stu-id="5df95-116">For the mipmap 2D scenario, the application can either flatten each sub-resource discretely and quickly use a 1D sub-allocation algorithm, or, use a more complicated 2D sub-allocation technique to minimize video memory utilization.</span></span> <span data-ttu-id="5df95-117">La prima tecnica dovrebbe essere usata più spesso perché è più semplice.</span><span class="sxs-lookup"><span data-stu-id="5df95-117">The first technique is expected to be used more often as it is simpler.</span></span> <span data-ttu-id="5df95-118">La seconda tecnica può essere utile quando si imballa dati su un disco o in una rete.</span><span class="sxs-lookup"><span data-stu-id="5df95-118">The second technique may be useful when packing data onto a disk or across a network.</span></span> <span data-ttu-id="5df95-119">In entrambi i casi, l'applicazione deve comunque chiamare le API di copia per ogni risorsa secondaria.</span><span class="sxs-lookup"><span data-stu-id="5df95-119">In either case, the application must still call the copy APIs for each sub-resource.</span></span>

``` syntax
// Prepare a pBitmap in memory, with bitmapWidth, bitmapHeight, and pixel format of DXGI_FORMAT_B8G8R8A8_UNORM. 
//
// Sub-allocate from the buffer for texture data.
//

D3D12_SUBRESOURCE_FOOTPRINT pitchedDesc = { 0 };
pitchedDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
pitchedDesc.Width = bitmapWidth;
pitchedDesc.Height = bitmapHeight;
pitchedDesc.Depth = 1;
pitchedDesc.RowPitch = Align(bitmapWidth * sizeof(DWORD), D3D12_TEXTURE_DATA_PITCH_ALIGNMENT);

//
// Note that the helper function UpdateSubresource in D3DX12.h, and ID3D12Device::GetCopyableFootprints 
// can help applications fill out D3D12_SUBRESOURCE_FOOTPRINT and D3D12_PLACED_SUBRESOURCE_FOOTPRINT structures.
//
// Refer to the D3D12 Code example for the previous section "Uploading Different Types of Resources"
// for the code for SuballocateFromBuffer.
//

SuballocateFromBuffer(
    pitchedDesc.Height * pitchedDesc.RowPitch,
    D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT
    );

D3D12_PLACED_SUBRESOURCE_FOOTPRINT placedTexture2D = { 0 };
placedTexture2D.Offset = m_pDataCur – m_pDataBegin;
placedTexture2D.Footprint = pitchedDesc;

//
// Copy texture data from DWORD* pBitmap->pixels to the buffer
//

for (UINT y = 0; y < bitmapHeight; y++)
{
  UINT8 *pScan = m_pDataBegin + placedTexture2D.Offset + y * pitchedDesc.RowPitch;
  memcpy( pScan, &(pBitmap->pixels[y * bitmapWidth]), sizeof(DWORD) * bitmapWidth );
}

//
// Create default texture2D resource.
//

D3D12_RESOURCE_DESC  textureDesc { ... };

CComPtr<ID3D12Resource> texture2D;
d3dDevice->CreateCommittedResource( 
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT), 
        D3D12_HEAP_FLAG_NONE, &textureDesc, 
        D3D12_RESOURCE_STATE_COPY_DEST, 
        nullptr, 
        IID_PPV_ARGS(&texture2D) );

//
// Copy heap data to texture2D.
//

commandList->CopyTextureRegion( 
        &CD3DX12_TEXTURE_COPY_LOCATION( texture2D, 0 ), 
        0, 0, 0, 
        &CD3DX12_TEXTURE_COPY_LOCATION( m_spUploadHeap, placedTexture2D ), 
        nullptr );
```

<span data-ttu-id="5df95-120">Si noti l'uso delle strutture helper [**CD3DX12 \_ HEAP \_ PROPERTIES**](cd3dx12-heap-properties.md) e [**CD3DX12 \_ TEXTURE COPY \_ \_ LOCATION**](cd3dx12-texture-copy-location.md)e dei metodi [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) e [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span><span class="sxs-lookup"><span data-stu-id="5df95-120">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_TEXTURE\_COPY\_LOCATION**](cd3dx12-texture-copy-location.md), and the methods [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) and [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span></span>

## <a name="copying"></a><span data-ttu-id="5df95-121">asincrona</span><span class="sxs-lookup"><span data-stu-id="5df95-121">Copying</span></span>

<span data-ttu-id="5df95-122">I metodi D3D12 consentono alle applicazioni di sostituire i dati D3D11 [**UpdateSubresource,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource) [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)e i dati iniziali della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5df95-122">D3D12 methods enable applications to replace D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion), and resource initial data.</span></span> <span data-ttu-id="5df95-123">Una singola sottorisorsa 3D dei dati di trama principale di riga può trovarsi nelle risorse del buffer.</span><span class="sxs-lookup"><span data-stu-id="5df95-123">A single 3D subresource worth of row-major texture data may be located in buffer resources.</span></span> <span data-ttu-id="5df95-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) può copiare i dati di trama dal buffer a una risorsa trama con un layout di trama sconosciuto e viceversa.</span><span class="sxs-lookup"><span data-stu-id="5df95-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) can copy that texture data from the buffer to a texture resource with an unknown texture layout, and vice versa.</span></span> <span data-ttu-id="5df95-125">Le applicazioni devono preferire questo tipo di tecnica per popolare le risorse GPU a cui si accede di frequente, creando buffer di grandi dimensioni in un heap UPLOAD durante la creazione delle risorse GPU a cui si accede di frequente in un heap DEFAULT senza accesso alla CPU.</span><span class="sxs-lookup"><span data-stu-id="5df95-125">Applications should prefer this type of technique to populate frequently accessed GPU resources, by creating large buffers in an UPLOAD heap while creating the frequently accessed GPU resources in a DEFAULT heap that has no CPU access.</span></span> <span data-ttu-id="5df95-126">Questa tecnica supporta in modo efficiente GPU discrete e le relative grandi quantità di memoria inaccessibile alla CPU, senza compromettere in genere le architetture UMA.</span><span class="sxs-lookup"><span data-stu-id="5df95-126">Such a technique efficiently supports discrete GPUs and their large amounts of CPU-inaccessible memory, without commonly impairing UMA architectures.</span></span>

<span data-ttu-id="5df95-127">Si notino le due costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="5df95-127">Note the following two constants:</span></span>

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [<span data-ttu-id="5df95-128">**FOOTPRINT DELLE SOTTORISORSE D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5df95-128">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [<span data-ttu-id="5df95-129">**FOOTPRINT DELLE SOTTORISORSE \_ \_ POSIZIONATE D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="5df95-129">**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [<span data-ttu-id="5df95-130">**PERCORSO COPIA TRAMA D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5df95-130">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [<span data-ttu-id="5df95-131">**TIPO DI COPIA TRAMA D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5df95-131">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [<span data-ttu-id="5df95-132">**ID3D12Device::GetCopyableFootprints**</span><span class="sxs-lookup"><span data-stu-id="5df95-132">**ID3D12Device::GetCopyableFootprints**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [<span data-ttu-id="5df95-133">**ID3D12GraphicsCommandList::CopyResource**</span><span class="sxs-lookup"><span data-stu-id="5df95-133">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="5df95-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="5df95-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="5df95-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="5df95-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="5df95-136">**ID3D12GraphicsCommandList::CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="5df95-136">**ID3D12GraphicsCommandList::CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="5df95-137">**ID3D12CommandQueue::UpdateTileMappings**</span><span class="sxs-lookup"><span data-stu-id="5df95-137">**ID3D12CommandQueue::UpdateTileMappings**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a><span data-ttu-id="5df95-138">Mapping e annullamento del mapping</span><span class="sxs-lookup"><span data-stu-id="5df95-138">Mapping and unmapping</span></span>

<span data-ttu-id="5df95-139">[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) e [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) possono essere chiamati da più thread in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="5df95-139">[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) can be called by multiple threads safely.</span></span> <span data-ttu-id="5df95-140">La prima chiamata a **Map** alloca un intervallo di indirizzi virtuali della CPU per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5df95-140">The first call to **Map** allocates a CPU virtual address range for the resource.</span></span> <span data-ttu-id="5df95-141">L'ultima chiamata **a Unmap** dealloca l'intervallo di indirizzi virtuali della CPU.</span><span class="sxs-lookup"><span data-stu-id="5df95-141">The last call to **Unmap** deallocates the CPU virtual address range.</span></span> <span data-ttu-id="5df95-142">L'indirizzo virtuale della CPU viene in genere restituito all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5df95-142">The CPU virtual address is commonly returned to the application.</span></span>

<span data-ttu-id="5df95-143">Ogni volta che i dati vengono passati tra CPU e GPU tramite risorse negli heap di readback, è necessario usare [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) e [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) per supportare tutti i sistemi in cui è supportato D3D12.</span><span class="sxs-lookup"><span data-stu-id="5df95-143">Whenever data is passed between the CPU and GPU through resources in readback heaps, [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) must be used to support all systems D3D12 is supported on.</span></span> <span data-ttu-id="5df95-144">Mantenendo gli intervalli il più possibile ristretti, si ottimizza l'efficienza nei sistemi che richiedono intervalli (vedere [**D3D12 \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span><span class="sxs-lookup"><span data-stu-id="5df95-144">Keeping the ranges as tight as possible maximizes efficiency on the systems that require ranges (refer to [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span></span>

<span data-ttu-id="5df95-145">Le prestazioni degli strumenti di debug traggono vantaggio [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)non solo dall'uso accurato degli intervalli in tutte le chiamate Map  /  [**Unmap,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) ma anche dalle applicazioni che annullano il mapping delle risorse quando non verranno più apportate modifiche alla CPU.</span><span class="sxs-lookup"><span data-stu-id="5df95-145">The performance of debugging tools benefit not only from the accurate usage of ranges on all [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) calls, but also from applications unmapping resources when CPU modifications will no longer be made.</span></span>

<span data-ttu-id="5df95-146">Il metodo D3D11 dell'uso [**di Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (con il parametro DISCARD impostato) per rinominare le risorse non è supportato in D3D12.</span><span class="sxs-lookup"><span data-stu-id="5df95-146">The D3D11 method of using [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (with the DISCARD parameter set) to rename resources is not supported in D3D12.</span></span> <span data-ttu-id="5df95-147">Le applicazioni devono implementare la ridenominazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5df95-147">Applications must implement resource renaming themselves.</span></span> <span data-ttu-id="5df95-148">Tutte **le chiamate** map sono implicitamente NO OVERWRITE e \_ multi-thread.</span><span class="sxs-lookup"><span data-stu-id="5df95-148">All **Map** calls are implicitly NO\_OVERWRITE and multi-threaded.</span></span> <span data-ttu-id="5df95-149">È responsabilità dell'applicazione assicurarsi che tutte le operazioni GPU pertinenti contenute negli elenchi di comandi siano completate prima dell'accesso ai dati con la CPU.</span><span class="sxs-lookup"><span data-stu-id="5df95-149">It is the application’s responsibility to ensure that any relevant GPU work contained in command lists is finished before the accessing data with the CPU.</span></span> <span data-ttu-id="5df95-150">Le chiamate D3D12 a **Map** non scaricano in modo implicito i buffer dei comandi né bloccano l'attesa del completamento del lavoro della GPU.</span><span class="sxs-lookup"><span data-stu-id="5df95-150">D3D12 calls to **Map** do not implicitly flush any command buffers, nor do they block waiting for the GPU to finish work.</span></span> <span data-ttu-id="5df95-151">Di conseguenza, **map** e [**unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) possono anche essere ottimizzati in alcuni scenari.</span><span class="sxs-lookup"><span data-stu-id="5df95-151">As a result, **Map** and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) may even be optimized out in some scenarios.</span></span>

## <a name="buffer-alignment"></a><span data-ttu-id="5df95-152">Allineamento del buffer</span><span class="sxs-lookup"><span data-stu-id="5df95-152">Buffer alignment</span></span>

<span data-ttu-id="5df95-153">Restrizioni di allineamento del buffer:</span><span class="sxs-lookup"><span data-stu-id="5df95-153">Buffer alignment restrictions:</span></span>

-   <span data-ttu-id="5df95-154">La copia lineare di sottorisorse deve essere allineata a 512 byte (con l'altezza della riga allineata ai byte D3D12 \_ TEXTURE \_ DATA PITCH \_ \_ ALIGNMENT).</span><span class="sxs-lookup"><span data-stu-id="5df95-154">Linear subresource copying must be aligned to 512 bytes (with the row pitch aligned to D3D12\_TEXTURE\_DATA\_PITCH\_ALIGNMENT bytes).</span></span>
-   <span data-ttu-id="5df95-155">Le operazioni di lettura dei dati costanti devono essere un multiplo di 256 byte dall'inizio dell'heap, ad esempio solo da indirizzi allineati a 256 byte.</span><span class="sxs-lookup"><span data-stu-id="5df95-155">Constant data reads must be a multiple of 256 bytes from the beginning of the heap (i.e. only from addresses that are 256-byte aligned).</span></span>
-   <span data-ttu-id="5df95-156">Le operazioni di lettura dei dati dell'indice devono essere un multiplo delle dimensioni del tipo di dati dell'indice, ad esempio solo da indirizzi allineati naturalmente per i dati.</span><span class="sxs-lookup"><span data-stu-id="5df95-156">Index data reads must be a multiple of the index data type size (i.e. only from addresses that are naturally aligned for the data).</span></span>
-   <span data-ttu-id="5df95-157">[**I dati ID3D12GraphicsCommandList::ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) devono essere da offset multipli di 4 (ad esempio solo da indirizzi allineati con DWORD).</span><span class="sxs-lookup"><span data-stu-id="5df95-157">[**ID3D12GraphicsCommandList::ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) data must be from offsets that are multiples of 4 (i.e. only from addresses that are DWORD aligned).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5df95-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5df95-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5df95-159">Sottoallocazione all'interno dei buffer</span><span class="sxs-lookup"><span data-stu-id="5df95-159">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 
