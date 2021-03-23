---
title: Caricamento di diversi tipi di risorse
description: Viene illustrato come utilizzare un buffer per caricare sia i dati del buffer costante che i dati del buffer dei vertici nella GPU e come suddividere e collocare correttamente i dati all'interno dei buffer.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2edca2cd9f4d3becf5036056a89f91c50f2c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104067"
---
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="dc641-103">Caricamento di diversi tipi di risorse</span><span class="sxs-lookup"><span data-stu-id="dc641-103">Uploading Different Types of Resources</span></span>

<span data-ttu-id="dc641-104">Viene illustrato come utilizzare un buffer per caricare sia i dati del buffer costante che i dati del buffer dei vertici nella GPU e come suddividere e collocare correttamente i dati all'interno dei buffer.</span><span class="sxs-lookup"><span data-stu-id="dc641-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="dc641-105">L'utilizzo di un singolo buffer aumenta la flessibilità di utilizzo della memoria e fornisce alle applicazioni un controllo più rigoroso sull'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="dc641-105">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="dc641-106">Mostra anche le differenze tra i modelli D3D11 e D3D12 per il caricamento di diversi tipi di risorse.</span><span class="sxs-lookup"><span data-stu-id="dc641-106">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span>

-   [<span data-ttu-id="dc641-107">Caricare tipi diversi di risorse</span><span class="sxs-lookup"><span data-stu-id="dc641-107">Upload Different Types of Resources</span></span>](#upload-different-types-of-resources)
    -   [<span data-ttu-id="dc641-108">Esempio di codice: D3D11</span><span class="sxs-lookup"><span data-stu-id="dc641-108">Code Example: D3D11</span></span>](#code-example-d3d11)
    -   [<span data-ttu-id="dc641-109">Esempio di codice: D3D12</span><span class="sxs-lookup"><span data-stu-id="dc641-109">Code Example: D3D12</span></span>](#code-example-d3d12)
-   [<span data-ttu-id="dc641-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="dc641-110">Constants</span></span>](#constants)
-   [<span data-ttu-id="dc641-111">Risorse</span><span class="sxs-lookup"><span data-stu-id="dc641-111">Resources</span></span>](#uploading-different-types-of-resources)
-   [<span data-ttu-id="dc641-112">Reflection delle dimensioni delle risorse</span><span class="sxs-lookup"><span data-stu-id="dc641-112">Resource size reflection</span></span>](#resource-size-reflection)
-   [<span data-ttu-id="dc641-113">Allineamento buffer</span><span class="sxs-lookup"><span data-stu-id="dc641-113">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="dc641-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc641-114">Related topics</span></span>](#related-topics)

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="dc641-115">Caricare tipi diversi di risorse</span><span class="sxs-lookup"><span data-stu-id="dc641-115">Upload Different Types of Resources</span></span>

<span data-ttu-id="dc641-116">In D3D12 le applicazioni creano un buffer per supportare diversi tipi di dati delle risorse per il caricamento e copiano i dati delle risorse nello stesso buffer in modo analogo per i dati di risorse differenti.</span><span class="sxs-lookup"><span data-stu-id="dc641-116">In D3D12, applications create one buffer to accommodate different types of resource data for uploading, and copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="dc641-117">Vengono quindi create visualizzazioni singole per associare i dati delle risorse alla pipeline grafica nel nuovo modello di associazione di risorse.</span><span class="sxs-lookup"><span data-stu-id="dc641-117">Individual views are then created to bind those resource data to the graphics pipeline in the new resource binding model.</span></span>

<span data-ttu-id="dc641-118">In D3D11, le applicazioni creano buffer distinti per i diversi tipi di dati delle risorse (si noti il diverso `BindFlags` usato nel codice di esempio d3d11 seguente), associando in modo esplicito ogni buffer delle risorse alla pipeline grafica e aggiornando i dati delle risorse con metodi diversi in base ai diversi tipi di risorse.</span><span class="sxs-lookup"><span data-stu-id="dc641-118">In D3D11, applications create separate buffers for different types of resource data (note the different `BindFlags` used in the D3D11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="dc641-119">In D3D12 e D3D11, le applicazioni devono usare solo le risorse di caricamento in cui la CPU scriverà i dati una sola volta e la GPU lo leggerà una volta.</span><span class="sxs-lookup"><span data-stu-id="dc641-119">In both D3D12 and D3D11, applications should only use upload resources where the CPU will write the data once and the GPU will read it once.</span></span> <span data-ttu-id="dc641-120">Se i dati vengono letti più volte dalla GPU, la GPU non leggerà i dati in modo lineare oppure il rendering sarà già limitato a una GPU.</span><span class="sxs-lookup"><span data-stu-id="dc641-120">If the GPU will read the data multiple times, the GPU will not read the data linearly, or the rendering is significantly GPU-limited already.</span></span> <span data-ttu-id="dc641-121">L'opzione migliore potrebbe consistere nell'usare [**ID3D12GraphicsCommandList:: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) o [**ID3D12GraphicsCommandList:: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) per copiare i dati del buffer di caricamento in una risorsa predefinita.</span><span class="sxs-lookup"><span data-stu-id="dc641-121">The better option may be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span> <span data-ttu-id="dc641-122">Una risorsa predefinita può risiedere nella memoria video fisica sulle GPU discrete.</span><span class="sxs-lookup"><span data-stu-id="dc641-122">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-d3d11"></a><span data-ttu-id="dc641-123">Esempio di codice: D3D11</span><span class="sxs-lookup"><span data-stu-id="dc641-123">Code Example: D3D11</span></span>

``` syntax
// D3D11: Separate buffers for each resource type.

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

### <a name="code-example-d3d12"></a><span data-ttu-id="dc641-124">Esempio di codice: D3D12</span><span class="sxs-lookup"><span data-stu-id="dc641-124">Code Example: D3D12</span></span>

``` syntax
// D3D12: One buffer to accommodate different types of resources

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

<span data-ttu-id="dc641-125">Si noti l'uso delle strutture helper [**CD3DX12 \_ \_ Proprietà heap**](cd3dx12-heap-properties.md) e [**CD3DX12 \_ Resource \_ desc**](cd3dx12-resource-desc.md).</span><span class="sxs-lookup"><span data-stu-id="dc641-125">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_RESOURCE\_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="dc641-126">Costanti</span><span class="sxs-lookup"><span data-stu-id="dc641-126">Constants</span></span>

<span data-ttu-id="dc641-127">Per impostare costanti, vertici e indici in un heap upload o readback, usare le API seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc641-127">To set constants, vertices and indexes within an Upload or Readback heap, use the following APIs:</span></span>

-   [<span data-ttu-id="dc641-128">**ID3D12Device::CreateConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="dc641-128">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="dc641-129">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="dc641-129">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="dc641-130">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="dc641-130">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="dc641-131">Risorse</span><span class="sxs-lookup"><span data-stu-id="dc641-131">Resources</span></span>

<span data-ttu-id="dc641-132">Le risorse sono il concetto di D3D che astrae l'utilizzo della memoria fisica della GPU.</span><span class="sxs-lookup"><span data-stu-id="dc641-132">Resources are the D3D concept which abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="dc641-133">Le risorse richiedono lo spazio degli indirizzi virtuali della GPU per accedere alla memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="dc641-133">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="dc641-134">La creazione di risorse è a thread libero.</span><span class="sxs-lookup"><span data-stu-id="dc641-134">Resource creation is free-threaded.</span></span>

<span data-ttu-id="dc641-135">Sono disponibili tre tipi di risorse per quanto riguarda la creazione e la flessibilità degli indirizzi virtuali in D3D12:</span><span class="sxs-lookup"><span data-stu-id="dc641-135">There are three types of resources with respect to virtual address creation and flexibility in D3D12:</span></span>

-   <span data-ttu-id="dc641-136">Risorse sottoposte a commit</span><span class="sxs-lookup"><span data-stu-id="dc641-136">Committed resources</span></span>

    <span data-ttu-id="dc641-137">Le risorse di cui è stato eseguito il commit sono l'idea più comune delle risorse D3D nelle generazioni.</span><span class="sxs-lookup"><span data-stu-id="dc641-137">Committed resources are the most common idea of D3D resources over the generations.</span></span> <span data-ttu-id="dc641-138">La creazione di una risorsa di questo tipo consente di allocare l'intervallo di indirizzi virtuali, un heap implicito sufficientemente grande da adattarsi all'intera risorsa ed eseguire il commit dell'intervallo di indirizzi virtuali nella memoria fisica incapsulata dall'heap.</span><span class="sxs-lookup"><span data-stu-id="dc641-138">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="dc641-139">Le proprietà dell'heap implicite devono essere passate per corrispondere alla parità funzionale con le versioni D3D precedenti.</span><span class="sxs-lookup"><span data-stu-id="dc641-139">The implicit heap properties must be passed to match functional parity with previous D3D versions.</span></span> <span data-ttu-id="dc641-140">Vedere [**ID3D12Device:: CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="dc641-140">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

-   <span data-ttu-id="dc641-141">Risorse riservate</span><span class="sxs-lookup"><span data-stu-id="dc641-141">Reserved resources</span></span>

    <span data-ttu-id="dc641-142">Le risorse riservate sono equivalenti alle risorse D3D11 affiancate.</span><span class="sxs-lookup"><span data-stu-id="dc641-142">Reserved resources are equivalent to D3D11 tiled resources.</span></span> <span data-ttu-id="dc641-143">Al momento della creazione, viene allocato solo un intervallo di indirizzi virtuali e non viene eseguito il mapping ad alcun heap.</span><span class="sxs-lookup"><span data-stu-id="dc641-143">On their creation, only a virtual address range is allocated and not mapped to any heap.</span></span> <span data-ttu-id="dc641-144">L'applicazione eseguirà il mapping di tali risorse agli heap in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="dc641-144">The application will map such resources to heaps later.</span></span> <span data-ttu-id="dc641-145">Le funzionalità di tali risorse sono attualmente invariate rispetto a D3D11, perché è possibile eseguirne il mapping a un heap a una granularità del riquadro 64KB con [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span><span class="sxs-lookup"><span data-stu-id="dc641-145">The capabilities of such resources are currently unchanged over D3D11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="dc641-146">Vedere [ **ID3D12Device:: CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span><span class="sxs-lookup"><span data-stu-id="dc641-146">Refer to [**ID3D12Device::CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span></span>

-   <span data-ttu-id="dc641-147">Risorse posizionate</span><span class="sxs-lookup"><span data-stu-id="dc641-147">Placed resources</span></span>

    <span data-ttu-id="dc641-148">Nuove per D3D12, le applicazioni possono creare heap distinti dalle risorse.</span><span class="sxs-lookup"><span data-stu-id="dc641-148">New for D3D12, applications may create heaps separate from resources.</span></span> <span data-ttu-id="dc641-149">Successivamente, l'applicazione può individuare più risorse all'interno di un singolo heap.</span><span class="sxs-lookup"><span data-stu-id="dc641-149">Afterward, the application may locate multiple resources within a single heap.</span></span> <span data-ttu-id="dc641-150">Questa operazione può essere eseguita senza creare risorse affiancate o riservate, abilitando le funzionalità per tutti i tipi di risorse che possono essere creati direttamente dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="dc641-150">This can be done without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by applications.</span></span> <span data-ttu-id="dc641-151">È possibile che più risorse si sovrappongano e che l'applicazione debba utilizzare `TiledResourceBarrier` per riutilizzare correttamente la memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="dc641-151">Multiple resources may overlap, and the application must use the `TiledResourceBarrier` to re-use physical memory correctly.</span></span> <span data-ttu-id="dc641-152">Vedere [ **ID3D12Device:: CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span><span class="sxs-lookup"><span data-stu-id="dc641-152">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="dc641-153">Reflection delle dimensioni delle risorse</span><span class="sxs-lookup"><span data-stu-id="dc641-153">Resource size reflection</span></span>

<span data-ttu-id="dc641-154">Le applicazioni devono usare la reflection delle dimensioni delle risorse per comprendere la quantità di trame della stanza con layout di trama sconosciuti richiesti negli heap.</span><span class="sxs-lookup"><span data-stu-id="dc641-154">Applications must use resource size reflection to understand how much room textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="dc641-155">Sono supportati anche i buffer, ma per lo più per praticità.</span><span class="sxs-lookup"><span data-stu-id="dc641-155">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="dc641-156">Le applicazioni devono essere a conoscenza delle principali discrepanze di allineamento, per aiutare a comprimere più densamente le risorse.</span><span class="sxs-lookup"><span data-stu-id="dc641-156">Applications should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="dc641-157">Ad esempio, una matrice a elemento singolo con un buffer a un byte restituisce una dimensione di 64KB e un allineamento di 64KB, in quanto i buffer attualmente possono essere allineati solo 64KB.</span><span class="sxs-lookup"><span data-stu-id="dc641-157">For example, a single-element array with a one-byte-buffer returns a Size of 64KB and an Alignment of 64KB, as buffers currently can only be 64KB aligned.</span></span>

<span data-ttu-id="dc641-158">Inoltre, una matrice a tre elementi con due trame allineate 64KB a Texel singolo e una trama a singolo Texel 4 bit allineata segnala dimensioni diverse in base all'ordine della matrice.</span><span class="sxs-lookup"><span data-stu-id="dc641-158">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="dc641-159">Se le trame da 4 MB sono allineate al centro, le dimensioni risultanti sono 12 MB.</span><span class="sxs-lookup"><span data-stu-id="dc641-159">If the 4MB aligned textures is in the middle, the resulting Size is 12MB.</span></span> <span data-ttu-id="dc641-160">In caso contrario, la dimensione risultante è 8 MB.</span><span class="sxs-lookup"><span data-stu-id="dc641-160">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="dc641-161">L'allineamento restituito sarà sempre di 4 MB, il super-set di tutti gli allineamenti nella matrice di risorse.</span><span class="sxs-lookup"><span data-stu-id="dc641-161">The Alignment returned would always be 4MB, the super-set of all alignments in the resource array.</span></span>

<span data-ttu-id="dc641-162">Fare riferimento alle seguenti API:</span><span class="sxs-lookup"><span data-stu-id="dc641-162">Reference the following APIs:</span></span>

-   [<span data-ttu-id="dc641-163">**\_Informazioni sull' \_ allocazione delle risorse D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="dc641-163">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
-   [<span data-ttu-id="dc641-164">**GetResourceAllocationInfo**</span><span class="sxs-lookup"><span data-stu-id="dc641-164">**GetResourceAllocationInfo**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="dc641-165">Allineamento buffer</span><span class="sxs-lookup"><span data-stu-id="dc641-165">Buffer alignment</span></span>

<span data-ttu-id="dc641-166">Le restrizioni di allineamento del buffer non sono state modificate da D3D11, in particolare:</span><span class="sxs-lookup"><span data-stu-id="dc641-166">Buffer alignment restrictions have not changed from D3D11, notably:</span></span>

-   <span data-ttu-id="dc641-167">4 MB per le trame multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="dc641-167">4 MB for multi-sample textures.</span></span>
-   <span data-ttu-id="dc641-168">64 KB per trame e buffer a singolo campione.</span><span class="sxs-lookup"><span data-stu-id="dc641-168">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc641-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc641-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc641-170">Sottoallocazione nei buffer</span><span class="sxs-lookup"><span data-stu-id="dc641-170">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




