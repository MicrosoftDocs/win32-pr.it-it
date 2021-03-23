---
title: Creazione di heap descrittore
description: Per creare e configurare un heap del descrittore, è necessario selezionare un tipo di heap del descrittore, determinare il numero di descrittori in esso contenuti e impostare i flag che indicano se si tratta di una CPU visibile e/o uno shader visibile.
ms.assetid: 58677023-692C-4BA4-90B7-D568F3DD3F73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e472a0749634d5cbaa9cbf1cde5e11202d4c4f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548801"
---
# <a name="creating-descriptor-heaps"></a><span data-ttu-id="56d41-103">Creazione di heap descrittore</span><span class="sxs-lookup"><span data-stu-id="56d41-103">Creating Descriptor Heaps</span></span>

<span data-ttu-id="56d41-104">Per creare e configurare un heap del descrittore, è necessario selezionare un tipo di heap del descrittore, determinare il numero di descrittori in esso contenuti e impostare i flag che indicano se si tratta di una CPU visibile e/o uno shader visibile.</span><span class="sxs-lookup"><span data-stu-id="56d41-104">To create and configure a descriptor heap, you must select a descriptor heap type, determine how many descriptors it contains, and set flags that indicate whether it is CPU visible and/or shader visible.</span></span>

-   [<span data-ttu-id="56d41-105">Tipi di heap del descrittore</span><span class="sxs-lookup"><span data-stu-id="56d41-105">Descriptor Heap types</span></span>](#descriptor-heap-types)
-   [<span data-ttu-id="56d41-106">Proprietà heap descrittore</span><span class="sxs-lookup"><span data-stu-id="56d41-106">Descriptor Heap Properties</span></span>](#descriptor-heap-properties)
-   [<span data-ttu-id="56d41-107">Handle del descrittore</span><span class="sxs-lookup"><span data-stu-id="56d41-107">Descriptor Handles</span></span>](#descriptor-handles)
-   [<span data-ttu-id="56d41-108">Metodi dell'heap del descrittore</span><span class="sxs-lookup"><span data-stu-id="56d41-108">Descriptor Heap Methods</span></span>](#descriptor-heap-methods)
-   [<span data-ttu-id="56d41-109">Wrapper dell'heap del descrittore minimo</span><span class="sxs-lookup"><span data-stu-id="56d41-109">Minimal descriptor heap wrapper</span></span>](#minimal-descriptor-heap-wrapper)
-   [<span data-ttu-id="56d41-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="56d41-110">Related topics</span></span>](#related-topics)

## <a name="descriptor-heap-types"></a><span data-ttu-id="56d41-111">Tipi di heap del descrittore</span><span class="sxs-lookup"><span data-stu-id="56d41-111">Descriptor Heap types</span></span>

<span data-ttu-id="56d41-112">Il tipo di heap è determinato da un membro dell'enumerazione [**del \_ \_ \_ tipo di heap del descrittore D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) :</span><span class="sxs-lookup"><span data-stu-id="56d41-112">The type of heap is determined by one member of the [**D3D12\_DESCRIPTOR\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) enum:</span></span>

``` syntax
typedef enum D3D12_DESCRIPTOR_HEAP_TYPE
{
    D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV,    // Constant buffer/Shader resource/Unordered access views
    D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER,        // Samplers
    D3D12_DESCRIPTOR_HEAP_TYPE_RTV,            // Render target view
    D3D12_DESCRIPTOR_HEAP_TYPE_DSV,            // Depth stencil view
    D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES       // Simply the number of descriptor heap types
} D3D12_DESCRIPTOR_HEAP_TYPE;
```

## <a name="descriptor-heap-properties"></a><span data-ttu-id="56d41-113">Proprietà heap descrittore</span><span class="sxs-lookup"><span data-stu-id="56d41-113">Descriptor Heap Properties</span></span>

<span data-ttu-id="56d41-114">Le proprietà dell'heap sono impostate sulla struttura [**\_ \_ \_ Desc del descrittore D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) , che fa riferimento sia alle enumerazioni del [**\_ \_ \_ tipo di heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) del descrittore di D3D12 sia alle enumerazioni dei [**\_ \_ \_ flag dell'heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="56d41-114">Heap properties are set on the [**D3D12\_DESCRIPTOR\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) structure, which references both the [**D3D12\_DESCRIPTOR\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) and [**D3D12\_DESCRIPTOR\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) enums.</span></span>

<span data-ttu-id="56d41-115">Il flag dell' \_ heap del descrittore D3D12 del flag \_ \_ \_ \_ visibile può facoltativamente essere impostato in un heap del descrittore per indicare che è associato a un elenco di comandi per riferimento da shader.</span><span class="sxs-lookup"><span data-stu-id="56d41-115">The flag D3D12\_DESCRIPTOR\_HEAP\_FLAG\_SHADER\_VISIBLE can optionally be set on a descriptor heap to indicate it is be bound on a command list for reference by shaders.</span></span> <span data-ttu-id="56d41-116">Gli heap del descrittore creati *senza* questo flag consentono alle applicazioni di organizzare i descrittori nella memoria della CPU prima di copiarli in un heap dei descrittori visibile dello shader, per praticità.</span><span class="sxs-lookup"><span data-stu-id="56d41-116">Descriptor heaps created *without* this flag allow applications the option to stage descriptors in CPU memory before copying them to a shader visible descriptor heap, as a convenience.</span></span> <span data-ttu-id="56d41-117">Tuttavia, le applicazioni possono anche creare direttamente i descrittori negli heap dei descrittori visibili dello shader senza alcun requisito per la gestione temporanea di qualsiasi elemento sulla CPU.</span><span class="sxs-lookup"><span data-stu-id="56d41-117">But it is also fine for applications to directly create descriptors into shader visible descriptor heaps with no requirement to stage anything on the CPU.</span></span>

<span data-ttu-id="56d41-118">Questo flag si applica solo a CBV, SRV, UAV e Samplers.</span><span class="sxs-lookup"><span data-stu-id="56d41-118">This flag only applies to CBV, SRV, UAV and samplers.</span></span> <span data-ttu-id="56d41-119">Non si applica ad altri tipi di heap del descrittore perché gli shader non fanno direttamente riferimento ad altri tipi.</span><span class="sxs-lookup"><span data-stu-id="56d41-119">It does not apply to other descriptor heap types since shaders do not directly reference the other types.</span></span>

<span data-ttu-id="56d41-120">Ad esempio, descrivere e creare un heap del descrittore del campionatore.</span><span class="sxs-lookup"><span data-stu-id="56d41-120">For example, describe and create a sampler descriptor heap.</span></span>


```C++
// Describe and create a sampler descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC samplerHeapDesc = {};
samplerHeapDesc.NumDescriptors = 1;
samplerHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER;
samplerHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&samplerHeapDesc, IID_PPV_ARGS(&m_samplerHeap)));
```



<span data-ttu-id="56d41-121">Descrivere e creare una visualizzazione buffer costante (CBV), una visualizzazione risorse shader (SRV) e un heap descrittore UAV (unordered Access View).</span><span class="sxs-lookup"><span data-stu-id="56d41-121">Describe and create a constant buffer view (CBV), Shader resource view (SRV), and unordered access view (UAV) descriptor heap.</span></span>


```C++
// Describe and create a shader resource view (SRV) and unordered
// access view (UAV) descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC srvUavHeapDesc = {};
srvUavHeapDesc.NumDescriptors = DescriptorCount;
srvUavHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
srvUavHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&srvUavHeapDesc, IID_PPV_ARGS(&m_srvUavHeap)));

m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
m_srvUavDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV);
```



## <a name="descriptor-handles"></a><span data-ttu-id="56d41-122">Handle del descrittore</span><span class="sxs-lookup"><span data-stu-id="56d41-122">Descriptor Handles</span></span>

<span data-ttu-id="56d41-123">Le strutture handle [**\_ \_ descrittore \_ GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) e [**\_ \_ descrittore \_ CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) identificano descrittori specifici in un heap del descrittore.</span><span class="sxs-lookup"><span data-stu-id="56d41-123">The [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) and [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structures identify specific descriptors in a descriptor heap.</span></span> <span data-ttu-id="56d41-124">Un handle è un bit come un puntatore, ma l'applicazione non deve dereferenziarla manualmente; in caso contrario, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="56d41-124">A handle is a bit like a pointer, but the application must not dereference it manually; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="56d41-125">L'uso degli handle deve passare attraverso l'API.</span><span class="sxs-lookup"><span data-stu-id="56d41-125">The use of the handles must go through the API.</span></span> <span data-ttu-id="56d41-126">Un handle può essere copiato liberamente o passato in API che operano in/usano i descrittori.</span><span class="sxs-lookup"><span data-stu-id="56d41-126">A handle itself can be copied freely or passed into APIs that operate on/use descriptors.</span></span> <span data-ttu-id="56d41-127">Non esiste un conteggio dei riferimenti, quindi l'applicazione deve assicurarsi che non usi un handle dopo l'eliminazione dell'heap del descrittore sottostante.</span><span class="sxs-lookup"><span data-stu-id="56d41-127">There is no ref counting, so the application must ensure that it does not use a handle after the underlying descriptor heap has been deleted.</span></span>

<span data-ttu-id="56d41-128">Le applicazioni possono individuare le dimensioni di incremento dei descrittori per un determinato tipo di heap del descrittore, in modo da poter generare manualmente gli handle in qualsiasi posizione in un heap del descrittore a partire dall'handle alla base.</span><span class="sxs-lookup"><span data-stu-id="56d41-128">Applications can find out the increment size of the descriptors for a given descriptor heap type, so that they can generate handles to any location in a descriptor heap manually starting from the handle to the base.</span></span> <span data-ttu-id="56d41-129">Le applicazioni non devono mai impostare come hardcoded le dimensioni di incremento dell'handle del descrittore e devono sempre eseguire una query per una determinata istanza del dispositivo. in caso contrario, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="56d41-129">Applications must never hardcode descriptor handle increment sizes, and should always query them for a given device instance; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="56d41-130">Le applicazioni non devono inoltre utilizzare le dimensioni e gli handle di incremento per eseguire i propri esami o la manipolazione dei dati dell'heap del descrittore, perché i risultati di tale operazione non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="56d41-130">Applications must also not use the increment sizes and handles to do their own examination or manipulation of descriptor heap data, as the results from doing so are undefined.</span></span> <span data-ttu-id="56d41-131">Gli handle possono non essere effettivamente usati come puntatori, bensì come proxy per i puntatori in modo da evitare la dereferenziazione accidentale.</span><span class="sxs-lookup"><span data-stu-id="56d41-131">The handles may not actually be used as pointers, but rather as proxies for pointers so as to avoid accidental dereferencing.</span></span>

> [!Note]
>
> <span data-ttu-id="56d41-132">È presente una struttura di supporto, \_ \_ handle descrittore GPU CD3DX12 \_ , definita nell'intestazione d3dx12. h, che eredita la struttura dell' [**\_ \_ \_ handle del descrittore della GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) e fornisce l'inizializzazione e altre operazioni utili.</span><span class="sxs-lookup"><span data-stu-id="56d41-132">There is a helper structure, CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, defined in the header d3dx12.h, which inherits the [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure and provides initialization and other useful operations.</span></span> <span data-ttu-id="56d41-133">Analogamente \_ , la \_ struttura di supporto del descrittore della CPU CD3DX12 \_ è definita per la struttura dell' [**\_ \_ \_ handle descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="56d41-133">Similarly the CD3DX12\_CPU\_DESCRIPTOR\_HANDLE helper structure is defined for the [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

 

<span data-ttu-id="56d41-134">Entrambe le strutture helper vengono utilizzate durante la compilazione degli elenchi di comandi.</span><span class="sxs-lookup"><span data-stu-id="56d41-134">Both of these helper structures are used when populating command lists.</span></span>


```C++
// Fill the command list with all the render commands and dependent state.
void D3D12nBodyGravity::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated
    // command lists have finished execution on the GPU; apps should use
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocators[m_frameIndex]->Reset());

    // However, when ExecuteCommandList() is called on a particular command
    // list, that command list can then be reset at any time and must be before
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocators[m_frameIndex].Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetPipelineState(m_pipelineState.Get());
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

    m_commandList->SetGraphicsRootConstantBufferView(RootParameterCB, m_constantBufferGS->GetGPUVirtualAddress() + m_frameIndex * sizeof(ConstantBufferGS));

    ID3D12DescriptorHeap* ppHeaps[] = { m_srvUavHeap.Get() };
    m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_POINTLIST);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.0f, 0.1f, 0.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);

    // Render the particles.
    float viewportHeight = static_cast<float>(static_cast<UINT>(m_viewport.Height) / m_heightInstances);
    float viewportWidth = static_cast<float>(static_cast<UINT>(m_viewport.Width) / m_widthInstances);
    for (UINT n = 0; n < ThreadCount; n++)
    {
        const UINT srvIndex = n + (m_srvIndex[n] == 0 ? SrvParticlePosVelo0 : SrvParticlePosVelo1);

        D3D12_VIEWPORT viewport;
        viewport.TopLeftX = (n % m_widthInstances) * viewportWidth;
        viewport.TopLeftY = (n / m_widthInstances) * viewportHeight;
        viewport.Width = viewportWidth;
        viewport.Height = viewportHeight;
        viewport.MinDepth = D3D12_MIN_DEPTH;
        viewport.MaxDepth = D3D12_MAX_DEPTH;
        m_commandList->RSSetViewports(1, &viewport);

        CD3DX12_GPU_DESCRIPTOR_HANDLE srvHandle(m_srvUavHeap->GetGPUDescriptorHandleForHeapStart(), srvIndex, m_srvUavDescriptorSize);
        m_commandList->SetGraphicsRootDescriptorTable(RootParameterSRV, srvHandle);

        m_commandList->DrawInstanced(ParticleCount, 1, 0, 0);
    }

    m_commandList->RSSetViewports(1, &m_viewport);

    // Indicate that the back buffer will now be used to present.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList->Close());
}
```



## <a name="descriptor-heap-methods"></a><span data-ttu-id="56d41-135">Metodi dell'heap del descrittore</span><span class="sxs-lookup"><span data-stu-id="56d41-135">Descriptor Heap Methods</span></span>

<span data-ttu-id="56d41-136">Gli heap dei descrittori ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) ereditano da [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable).</span><span class="sxs-lookup"><span data-stu-id="56d41-136">Descriptor heaps ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) inherit from [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable).</span></span> <span data-ttu-id="56d41-137">Ciò impone la responsabilità della gestione della residenza degli heap del descrittore nelle applicazioni, proprio come gli heap delle risorse.</span><span class="sxs-lookup"><span data-stu-id="56d41-137">This imposes the responsibility for the residency management of descriptor heaps on applications, just like resource heaps.</span></span> <span data-ttu-id="56d41-138">I metodi di gestione della residenza si applicano solo agli heap visibili dello shader poiché gli heap visibili non shader non sono visibili direttamente alla GPU.</span><span class="sxs-lookup"><span data-stu-id="56d41-138">The residency management methods only apply to shader visible heaps since the non shader visible heaps are not visible to the GPU directly.</span></span>

<span data-ttu-id="56d41-139">Il metodo [**ID3D12Device:: GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) consente alle applicazioni di eseguire manualmente l'offset degli handle in un heap (generando handle in un punto qualsiasi in un heap del descrittore).</span><span class="sxs-lookup"><span data-stu-id="56d41-139">The [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) method allows applications to manually offset handles into a heap (producing handles into anywhere in a descriptor heap).</span></span> <span data-ttu-id="56d41-140">Il punto di controllo dell'inizio dell'heap deriva da [**ID3D12DescriptorHeap:: GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) / [**ID3D12DescriptorHeap:: GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart).</span><span class="sxs-lookup"><span data-stu-id="56d41-140">The heap start location’s handle comes from [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)/[**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart).</span></span> <span data-ttu-id="56d41-141">La compensazione viene eseguita aggiungendo le dimensioni di incremento \* del numero di descrittori da compensare all'inizio dell'heap del descrittore.</span><span class="sxs-lookup"><span data-stu-id="56d41-141">Offsetting is done by adding the increment size \* the number of descriptors to offset to the descriptor heap start .</span></span> <span data-ttu-id="56d41-142">Si noti che la dimensione di incremento non può essere considerata come una dimensione in byte poiché le applicazioni non devono dereferenziare gli handle come se fossero memoria: la memoria a cui puntava ha un layout non standardizzato e può variare anche per un determinato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56d41-142">Note that the increment size cannot be thought of as a byte size since applications must not dereference handles as if they are memory – the memory pointed to has a non-standardized layout and can vary even for a given device.</span></span>

<span data-ttu-id="56d41-143">[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) restituisce un handle CPU per gli heap del descrittore visibile della CPU.</span><span class="sxs-lookup"><span data-stu-id="56d41-143">[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) returns a CPU handle for CPU visible descriptor heaps.</span></span> <span data-ttu-id="56d41-144">Restituisce un handle NULL (e il livello di debug segnalerà un errore) se l'heap del descrittore non è visibile alla CPU.</span><span class="sxs-lookup"><span data-stu-id="56d41-144">It returns a NULL handle (and the debug layer will report an error) if the descriptor heap is not CPU visible.</span></span>

<span data-ttu-id="56d41-145">[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) restituisce un handle GPU per gli heap del descrittore visibile dello shader.</span><span class="sxs-lookup"><span data-stu-id="56d41-145">[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) returns a GPU handle for shader visible descriptor heaps.</span></span> <span data-ttu-id="56d41-146">Restituisce un handle NULL (e il livello di debug segnalerà un errore) se l'heap del descrittore non è visibile.</span><span class="sxs-lookup"><span data-stu-id="56d41-146">It returns a NULL handle (and the debug layer will report an error) if the descriptor heap is not shader visible.</span></span>

<span data-ttu-id="56d41-147">Ad esempio, creazione di visualizzazioni di destinazione di rendering per visualizzare il testo D2D usando un dispositivo 11on12.</span><span class="sxs-lookup"><span data-stu-id="56d41-147">For example, creating render target views to display D2D text using an 11on12 device.</span></span>


```C++
    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_d3d12Device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_d3d12Device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    
    }
```



## <a name="minimal-descriptor-heap-wrapper"></a><span data-ttu-id="56d41-148">Wrapper dell'heap del descrittore minimo</span><span class="sxs-lookup"><span data-stu-id="56d41-148">Minimal descriptor heap wrapper</span></span>

<span data-ttu-id="56d41-149">È probabile che gli sviluppatori di applicazioni desiderino compilare il proprio codice di supporto per la gestione degli heap e degli handle del descrittore.</span><span class="sxs-lookup"><span data-stu-id="56d41-149">Application developers will likely want to build their own helper code for managing descriptor handles and heaps.</span></span> <span data-ttu-id="56d41-150">Di seguito è riportato un esempio di base.</span><span class="sxs-lookup"><span data-stu-id="56d41-150">A basic example is shown below.</span></span> <span data-ttu-id="56d41-151">I wrapper più sofisticati potrebbero, ad esempio, tenere traccia dei tipi di descrittori che si trovano in un heap e archiviano gli argomenti di creazione del descrittore.</span><span class="sxs-lookup"><span data-stu-id="56d41-151">More sophisticated wrappers could, for example, keep track of what types of descriptors are where in a heap and store the descriptor creation arguments.</span></span>

``` syntax
class CDescriptorHeapWrapper
{
public:
    CDescriptorHeapWrapper() { memset(this, 0, sizeof(*this)); }

    HRESULT Create(
        ID3D12Device* pDevice, 
        D3D12_DESCRIPTOR_HEAP_TYPE Type, 
        UINT NumDescriptors, 
        bool bShaderVisible = false)
    {
        D3D12_DESCRIPTOR_HEAP_DESC Desc;
        Desc.Type = Type;
        Desc.NumDescriptors = NumDescriptors;
        Desc.Flags = (bShaderVisible ? D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE : D3D12_DESCRIPTOR_HEAP_FLAG_NONE);
       
        HRESULT hr = pDevice->CreateDescriptorHeap(&Desc, 
                               __uuidof(ID3D12DescriptorHeap), 
                               (void**)&pDH);
        if (FAILED(hr)) return hr;

        hCPUHeapStart = pDH->GetCPUDescriptorHandleForHeapStart();
        hGPUHeapStart = pDH->GetGPUDescriptorHandleForHeapStart();

        HandleIncrementSize = pDevice->GetDescriptorHandleIncrementSize(Desc.Type);
        return hr;
    }
    operator ID3D12DescriptorHeap*() { return pDH; }

    D3D12_CPU_DESCRIPTOR_HANDLE hCPU(UINT index)
    {
        return hCPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_GPU_DESCRIPTOR_HANDLE hGPU(UINT index) 
    {
        assert(Desc.Flags&D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE); 
        return hGPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_DESCRIPTOR_HEAP_DESC Desc;
    CComPtr<ID3D12DescriptorHeap> pDH;
    D3D12_CPU_DESCRIPTOR_HANDLE hCPUHeapStart;
    D3D12_GPU_DESCRIPTOR_HANDLE hGPUHeapStart;
    UINT HandleIncrementSize;
};
```

## <a name="related-topics"></a><span data-ttu-id="56d41-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="56d41-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56d41-153">Heap descrittore</span><span class="sxs-lookup"><span data-stu-id="56d41-153">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 