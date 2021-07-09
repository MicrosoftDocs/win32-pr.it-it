---
title: Caricamento di diversi tipi di risorse
description: Illustra come usare un buffer per caricare sia i dati costanti del buffer che i dati del buffer dei vertici nella GPU e come sottoallocare e inserire correttamente i dati all'interno dei buffer.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03d4755124bbadcdd255a6e99739b710845ab14
ms.sourcegitcommit: a30d0436a84986234df673c6def6694d5a8579f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113563781"
---
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="b90bf-103">Caricamento di diversi tipi di risorse</span><span class="sxs-lookup"><span data-stu-id="b90bf-103">Uploading different types of resources</span></span>

<span data-ttu-id="b90bf-104">Illustra come usare un buffer per caricare sia i dati costanti del buffer che i dati del buffer dei vertici nella GPU e come sottoallocare e inserire correttamente i dati all'interno dei buffer.</span><span class="sxs-lookup"><span data-stu-id="b90bf-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="b90bf-105">L'uso di un singolo buffer aumenta la flessibilità di utilizzo della memoria e offre alle applicazioni un controllo più stretto sull'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="b90bf-105">The use of a single buffer increases memory usage flexibility, and provides applications with tighter control over memory usage.</span></span> <span data-ttu-id="b90bf-106">Illustra anche le differenze tra i modelli Direct3D 11 e Direct3D 12 per il caricamento di diversi tipi di risorse.</span><span class="sxs-lookup"><span data-stu-id="b90bf-106">Also shows the differences between the Direct3D 11 and Direct3D 12 models for uploading different types of resources.</span></span>

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="b90bf-107">Upload diversi tipi di risorse</span><span class="sxs-lookup"><span data-stu-id="b90bf-107">Upload different types of resources</span></span>

<span data-ttu-id="b90bf-108">In Direct3D 12 si crea un buffer per supportare diversi tipi di dati delle risorse per il caricamento e si copiano i dati delle risorse nello stesso buffer in modo simile per dati di risorse diversi.</span><span class="sxs-lookup"><span data-stu-id="b90bf-108">In Direct3D 12, you create one buffer to accommodate different types of resource data for uploading, and you copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="b90bf-109">Vengono quindi create singole visualizzazioni per associare i dati delle risorse alla pipeline grafica nel modello di associazione di risorse Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="b90bf-109">Individual views are then created to bind those resource data to the graphics pipeline in the Direct3D 12 resource binding model.</span></span>

<span data-ttu-id="b90bf-110">In Direct3D 11 si creano buffer separati per diversi tipi di dati delle risorse (si noti il diverso usato nel codice di esempio Direct3D 11 riportato di seguito), si associa in modo esplicito ogni buffer di risorse alla pipeline grafica e si aggiornano i dati delle risorse con metodi diversi in base a tipi di `BindFlags` risorse diversi.</span><span class="sxs-lookup"><span data-stu-id="b90bf-110">In Direct3D 11, you create separate buffers for different types of resource data (note the different `BindFlags` used in the Direct3D 11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="b90bf-111">Sia in Direct3D 12 che in Direct3D 11 è consigliabile caricare le risorse solo dove la CPU scriverà i dati una sola volta e la GPU la leggerà una sola volta.</span><span class="sxs-lookup"><span data-stu-id="b90bf-111">In both Direct3D 12 and Direct3D 11, you should use upload resources only where the CPU will write the data once, and the GPU will read it once.</span></span>

<span data-ttu-id="b90bf-112">In alcuni casi,</span><span class="sxs-lookup"><span data-stu-id="b90bf-112">In some cases,</span></span>
* <span data-ttu-id="b90bf-113">la GPU leggerà i dati più volte oppure</span><span class="sxs-lookup"><span data-stu-id="b90bf-113">the GPU will read the data multiple times, or</span></span>
* <span data-ttu-id="b90bf-114">la GPU non leggerà i dati in modo lineare o</span><span class="sxs-lookup"><span data-stu-id="b90bf-114">the GPU won't read the data linearly, or</span></span>
* <span data-ttu-id="b90bf-115">il rendering è già notevolmente limitato alla GPU.</span><span class="sxs-lookup"><span data-stu-id="b90bf-115">the rendering is significantly GPU-limited already.</span></span>

<span data-ttu-id="b90bf-116">In questi casi, l'opzione migliore potrebbe essere usare [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) o [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) per copiare i dati del buffer di caricamento in una risorsa predefinita.</span><span class="sxs-lookup"><span data-stu-id="b90bf-116">In those cases, the better option might be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span>

<span data-ttu-id="b90bf-117">Una risorsa predefinita può risiedere nella memoria video fisica in GPU discrete.</span><span class="sxs-lookup"><span data-stu-id="b90bf-117">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-direct3d-11"></a><span data-ttu-id="b90bf-118">Esempio di codice: Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="b90bf-118">Code Example: Direct3D 11</span></span>

```cpp
// Direct3D 11: Separate buffers for each resource type.

void main()
{
    // ...

    // Create a constant buffer.
    float constantBufferData[] = ...;

    D3D11_BUFFER_DESC constantBufferDesc = {0};  
    constantBufferDesc.ByteWidth = sizeof(constantBufferData);  
    constantBufferDesc.Usage = D3D11_USAGE_DYNAMIC;  
    constantBufferDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;  
    constantBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;  

    ComPtr<ID3D11Buffer> constantBuffer;
    d3dDevice->CreateBuffer(  
        &constantBufferDesc,  
        NULL,
        &constantBuffer  
        );

    // Create a vertex buffer.
    float vertexBufferData[] = ...;

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(vertexBufferData);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;

    ComPtr<ID3D11Buffer> vertexBuffer;
    d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        NULL,
        &vertexBuffer
        );

    // ...
}

void DrawFrame()
{
    // ...

    // Bind buffers to the graphics pipeline.
    d3dDeviceContext->VSSetConstantBuffers(0, 1, constantBuffer.Get());
    d3dDeviceContext->IASetVertexBuffers(0, 1, vertexBuffer.Get(), ...);

    // Update the constant buffer.
    D3D11_MAPPED_SUBRESOURCE mappedResource;  
    d3dDeviceContext->Map(
        constantBuffer.Get(),
        0, 
        D3D11_MAP_WRITE_DISCARD,
        0,
        &mappedResource
        );
    memcpy(mappedResource.pData, constantBufferData,
        sizeof(contatnBufferData));
    d3dDeviceContext->Unmap(constantBuffer.Get(), 0);  

    // Update the vertex buffer.
    d3dDeviceContext->UpdateSubresource(
        vertexBuffer.Get(),
        0,
        NULL,
        vertexBufferData,
        sizeof(vertexBufferData),
        0
    );

    // ...
}
```

### <a name="code-example-direct3d-12"></a><span data-ttu-id="b90bf-119">Esempio di codice: Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b90bf-119">Code Example: Direct3D 12</span></span>

```cpp
// Direct3D 12: One buffer to accommodate different types of resources

ComPtr<ID3D12Resource> m_spUploadBuffer;
UINT8* m_pDataBegin = nullptr;    // starting position of upload buffer
UINT8* m_pDataCur = nullptr;      // current position of upload buffer
UINT8* m_pDataEnd = nullptr;      // ending position of upload buffer

void main()
{
    //
    // Initialize an upload buffer
    //

    InitializeUploadBuffer(64 * 1024);

    // ...
}

void DrawFrame()
{
    // ...

    // Set vertices data to the upload buffer.

    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float),
            sizeof(float), 
            verticesOffset
            ));

    // Set constant data to the upload buffer.

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT, 
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model.

    D3D12_VERTEX_BUFFER_VIEW vertexBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + verticesOffset,
        sizeof(vertices), // size
        sizeof(float) * 4,  // stride
    };

    commandList->IASetVertexBuffers( 
        0,
        1,
        &vertexBufferViewDesc,
        ));

    // Create constant buffer views for the new binding model.

    D3D12_CONSTANT_BUFFER_VIEW_DESC constantBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + constantsOffset,
        sizeof(constants) // size
         };

    d3dDevice->CreateConstantBufferView(
        &constantBufferViewDesc,
        ...
        ));

    // Continue command list building and execution ...
}

//
// Create an upload buffer and keep it always mapped.
//

HRESULT InitializeUploadBuffer(SIZE_T uSize)
{
    HRESULT hr = d3dDevice->CreateCommittedResource(
         &CD3DX12_HEAP_PROPERTIES( D3D12_HEAP_TYPE_UPLOAD ),    
               D3D12_HEAP_FLAG_NONE, 
               &CD3DX12_RESOURCE_DESC::Buffer( uSize ), 
               D3D12_RESOURCE_STATE_GENERIC_READ, nullptr,  
               IID_PPV_ARGS( &m_spUploadBuffer ) );

    if (SUCCEEDED(hr))
    {
        void* pData;
        //
        // No CPU reads will be done from the resource.
        //
        CD3DX12_RANGE readRange(0, 0);
        m_spUploadBuffer->Map( 0, &readRange, &pData ); 
        m_pDataCur = m_pDataBegin = reinterpret_cast< UINT8* >( pData );
        m_pDataEnd = m_pDataBegin + uSize;
    }
    return hr;
}

//
// Sub-allocate from the buffer, with offset aligned.
//

HRESULT SuballocateFromBuffer(SIZE_T uSize, UINT uAlign)
{
    m_pDataCur = reinterpret_cast< UINT8* >(
        Align(reinterpret_cast< SIZE_T >(m_pDataCur), uAlign)
        );

    return (m_pDataCur + uSize > m_pDataEnd) ? E_INVALIDARG : S_OK;
}

//
// Place and copy data to the upload buffer.
//

HRESULT SetDataToUploadBuffer(
    const void* pData, 
    UINT bytesPerData, 
    UINT dataCount, 
    UINT alignment, 
    UINT& byteOffset
    )
{
    SIZE_T byteSize = bytesPerData * dataCount;
    HRESULT hr = SuballocateFromBuffer(byteSize, alignment);
    if (SUCCEEDED(hr))
    {
        byteOffset = UINT(m_pDataCur - m_pDataBegin);
        memcpy(m_pDataCur, pData, byteSize); 
        m_pDataCur += byteSize;
    }
    return hr;
}

//
// Align uLocation to the next multiple of uAlign.
//

UINT Align(UINT uLocation, UINT uAlign)
{
    if ( (0 == uAlign) || (uAlign & (uAlign-1)) )
    {
        ThrowException("non-pow2 alignment");
    }

    return ( (uLocation + (uAlign-1)) & ~(uAlign-1) );
}
```

<span data-ttu-id="b90bf-120">Si noti l'uso delle strutture helper [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) e [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).</span><span class="sxs-lookup"><span data-stu-id="b90bf-120">Note the use of the helper structures [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="b90bf-121">Costanti</span><span class="sxs-lookup"><span data-stu-id="b90bf-121">Constants</span></span>

<span data-ttu-id="b90bf-122">Per impostare costanti, vertici e indici all'interno di un heap di caricamento o readback, usare le API seguenti.</span><span class="sxs-lookup"><span data-stu-id="b90bf-122">To set constants, vertices, and indexes within an upload or readback heap, use the following APIs.</span></span>

-   [<span data-ttu-id="b90bf-123">**ID3D12Device::CreateConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="b90bf-123">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="b90bf-124">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="b90bf-124">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="b90bf-125">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="b90bf-125">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="b90bf-126">Risorse</span><span class="sxs-lookup"><span data-stu-id="b90bf-126">Resources</span></span>

<span data-ttu-id="b90bf-127">Le risorse sono il concetto direct3D che astrae l'utilizzo della memoria fisica GPU.</span><span class="sxs-lookup"><span data-stu-id="b90bf-127">Resources are the Direct3D concept that abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="b90bf-128">Le risorse richiedono lo spazio degli indirizzi virtuali GPU per accedere alla memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="b90bf-128">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="b90bf-129">La creazione di risorse è a thread libero.</span><span class="sxs-lookup"><span data-stu-id="b90bf-129">Resource creation is free-threaded.</span></span>

<span data-ttu-id="b90bf-130">Esistono tre tipi di risorse per quanto riguarda la creazione di indirizzi virtuali e la flessibilità in Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="b90bf-130">There are three types of resources with respect to virtual address creation and flexibility in Direct3D 12.</span></span>

### <a name="committed-resources"></a><span data-ttu-id="b90bf-131">Risorse di cui è stato eseguito il commit</span><span class="sxs-lookup"><span data-stu-id="b90bf-131">Committed resources</span></span>

<span data-ttu-id="b90bf-132">Le risorse di cui è stato eseguito il commit sono l'idea più comune di risorse Direct3D nelle generazioni.</span><span class="sxs-lookup"><span data-stu-id="b90bf-132">Committed resources are the most common idea of Direct3D resources over the generations.</span></span> <span data-ttu-id="b90bf-133">La creazione di una risorsa di questo tipo alloca un intervallo di indirizzi virtuali, un heap implicito sufficientemente grande da adattarsi all'intera risorsa ed esegue il commit dell'intervallo di indirizzi virtuali nella memoria fisica incapsulata dall'heap.</span><span class="sxs-lookup"><span data-stu-id="b90bf-133">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="b90bf-134">Le proprietà heap implicite devono essere passate in modo che corrispondano alla parità funzionale con le versioni precedenti di Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b90bf-134">The implicit heap properties must be passed to match functional parity with previous Direct3D versions.</span></span> <span data-ttu-id="b90bf-135">Vedere [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="b90bf-135">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

### <a name="reserved-resources"></a><span data-ttu-id="b90bf-136">Risorse riservate</span><span class="sxs-lookup"><span data-stu-id="b90bf-136">Reserved resources</span></span>

<span data-ttu-id="b90bf-137">Le risorse riservate sono equivalenti alle risorse affiancate Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="b90bf-137">Reserved resources are equivalent to Direct3D 11 tiled resources.</span></span> <span data-ttu-id="b90bf-138">Al momento della creazione, viene allocato solo un intervallo di indirizzi virtuali e non ne viene eseguito il mapping ad alcun heap.</span><span class="sxs-lookup"><span data-stu-id="b90bf-138">On their creation, only a virtual address range is allocated, and not mapped to any heap.</span></span> <span data-ttu-id="b90bf-139">L'applicazione esegue il mapping di tali risorse agli heap in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="b90bf-139">The application will map such resources to heaps later.</span></span> <span data-ttu-id="b90bf-140">Le funzionalità di tali risorse sono attualmente invariate rispetto a Direct3D 11, perché possono essere mappate a un heap con una granularità del riquadro di 64 KB con [**UpdateTileMappings.**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)</span><span class="sxs-lookup"><span data-stu-id="b90bf-140">The capabilities of such resources are currently unchanged from Direct3D 11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="b90bf-141">Vedere [**ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span><span class="sxs-lookup"><span data-stu-id="b90bf-141">Refer to [**ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span></span>

### <a name="placed-resources"></a><span data-ttu-id="b90bf-142">Risorse posizionate</span><span class="sxs-lookup"><span data-stu-id="b90bf-142">Placed resources</span></span>

<span data-ttu-id="b90bf-143">Una novità di Direct3D 12 è la creazione di heap separati dalle risorse.</span><span class="sxs-lookup"><span data-stu-id="b90bf-143">New for Direct3D 12, you can create heaps separate from resources.</span></span> <span data-ttu-id="b90bf-144">Successivamente, è possibile individuare più risorse all'interno di un singolo heap.</span><span class="sxs-lookup"><span data-stu-id="b90bf-144">Afterward, you can locate multiple resources within a single heap.</span></span> <span data-ttu-id="b90bf-145">È possibile farlo senza creare risorse affiancate o riservate, abilitando le funzionalità per tutti i tipi di risorse che possono essere create direttamente dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b90bf-145">You can do that without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by your application.</span></span> <span data-ttu-id="b90bf-146">È possibile che più risorse si sovrappongano ed è necessario usare [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) per usare di nuovo correttamente la memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="b90bf-146">Multiple resources might overlap, and you must use the [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to re-use physical memory correctly.</span></span> <span data-ttu-id="b90bf-147">Fare riferimento [**a ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span><span class="sxs-lookup"><span data-stu-id="b90bf-147">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="b90bf-148">Reflection delle dimensioni delle risorse</span><span class="sxs-lookup"><span data-stu-id="b90bf-148">Resource size reflection</span></span>

<span data-ttu-id="b90bf-149">È necessario usare la reflection delle dimensioni delle risorse per comprendere la quantità di trame di spazio con layout di trama sconosciuti necessari negli heap.</span><span class="sxs-lookup"><span data-stu-id="b90bf-149">You must use resource size reflection to understand how much space textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="b90bf-150">Sono supportati anche i buffer, ma soprattutto per praticità.</span><span class="sxs-lookup"><span data-stu-id="b90bf-150">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="b90bf-151">È necessario essere a conoscenza delle principali discrepanze di allineamento, per facilitare la creazione di un pacchetto di risorse più denso.</span><span class="sxs-lookup"><span data-stu-id="b90bf-151">You should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="b90bf-152">Ad esempio, una matrice a elemento singolo con  un buffer a un byte restituisce dimensioni di 64 KB e *allineamento* di 64 KB, perché i buffer possono essere allineati solo a 64 KB.</span><span class="sxs-lookup"><span data-stu-id="b90bf-152">For example, a single-element array with a one-byte-buffer returns a *Size* of 64KB, and an *Alignment* of 64KB, because buffers can be only 64KB-aligned.</span></span>

<span data-ttu-id="b90bf-153">Inoltre, una matrice a tre elementi con due trame allineate a 64 KB a texel singolo e una trama allineata a 4 MB a texel singolo segnala dimensioni diverse in base all'ordine della matrice.</span><span class="sxs-lookup"><span data-stu-id="b90bf-153">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="b90bf-154">Se le trame allineate a 4 MB si trova al centro, la dimensione *risultante* è 12 MB.</span><span class="sxs-lookup"><span data-stu-id="b90bf-154">If the 4MB aligned textures is in the middle, then the resulting *Size* is 12MB.</span></span> <span data-ttu-id="b90bf-155">In caso contrario, la dimensione risultante è 8 MB.</span><span class="sxs-lookup"><span data-stu-id="b90bf-155">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="b90bf-156">L'allineamento restituito sarebbe sempre di 4 MB, il superset di tutti gli allineamenti nella matrice di risorse.</span><span class="sxs-lookup"><span data-stu-id="b90bf-156">The Alignment returned would always be 4MB, the superset of all alignments in the resource array.</span></span>

<span data-ttu-id="b90bf-157">Fare riferimento alle API seguenti.</span><span class="sxs-lookup"><span data-stu-id="b90bf-157">Reference the following APIs.</span></span>

- [<span data-ttu-id="b90bf-158">**INFORMAZIONI SULL'ALLOCAZIONE DELLE RISORSE D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b90bf-158">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
- [<span data-ttu-id="b90bf-159">**GetResourceAllocationInfo**</span><span class="sxs-lookup"><span data-stu-id="b90bf-159">**GetResourceAllocationInfo**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="b90bf-160">Allineamento del buffer</span><span class="sxs-lookup"><span data-stu-id="b90bf-160">Buffer alignment</span></span>

<span data-ttu-id="b90bf-161">Le restrizioni di allineamento del buffer non sono cambiate rispetto a Direct3D 11, in particolare:</span><span class="sxs-lookup"><span data-stu-id="b90bf-161">Buffer alignment restrictions have not changed from Direct3D 11, notably:</span></span>

- <span data-ttu-id="b90bf-162">4 MB per trame multi-campione.</span><span class="sxs-lookup"><span data-stu-id="b90bf-162">4 MB for multi-sample textures.</span></span>
- <span data-ttu-id="b90bf-163">64 KB per trame e buffer a campione singolo.</span><span class="sxs-lookup"><span data-stu-id="b90bf-163">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b90bf-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b90bf-164">Related topics</span></span>

* [<span data-ttu-id="b90bf-165">Sottoallocazione all'interno dei buffer</span><span class="sxs-lookup"><span data-stu-id="b90bf-165">Suballocation within buffers</span></span>](large-buffers.md)
