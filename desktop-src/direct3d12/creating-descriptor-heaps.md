---
title: Creazione di heap dei descrittori
description: Per creare e configurare un heap descrittore, è necessario selezionare un tipo di heap descrittore, determinare il numero di descrittori in esso contenuti e impostare flag che indicano se è visibile alla CPU e/o shader.
ms.assetid: 58677023-692C-4BA4-90B7-D568F3DD3F73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d21d462dd393360e9ebfcb07ab5b35524b9d8d8c01c8ab1ef28ef90166eb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857991"
---
# <a name="creating-descriptor-heaps"></a>Creazione di heap dei descrittori

Per creare e configurare un heap descrittore, è necessario selezionare un tipo di heap descrittore, determinare il numero di descrittori in esso contenuti e impostare flag che indicano se è visibile alla CPU e/o shader.

-   [Tipi di heap del descrittore](#descriptor-heap-types)
-   [Proprietà dell'heap dei descrittori](#descriptor-heap-properties)
-   [Handle del descrittore](#descriptor-handles)
-   [Metodi dell'heap dei descrittori](#descriptor-heap-methods)
-   [Wrapper heap del descrittore minimo](#minimal-descriptor-heap-wrapper)
-   [Argomenti correlati](#related-topics)

## <a name="descriptor-heap-types"></a>Tipi di heap del descrittore

Il tipo di heap è determinato da un membro dell'enumerazione [**D3D12 \_ DESCRIPTOR \_ HEAP \_ TYPE:**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type)

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

## <a name="descriptor-heap-properties"></a>Proprietà dell'heap dei descrittori

Le proprietà dell'heap vengono impostate sulla struttura [**\_ \_ \_ DESC HEAP DESCRIPTOR D3D12,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) che fa riferimento sia alle enumerazioni [**D3D12 \_ DESCRIPTOR \_ HEAP \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) che [**D3D12 \_ DESCRIPTOR \_ HEAP \_ FLAGS.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)

Il flag D3D12 DESCRIPTOR HEAP FLAG SHADER VISIBLE può essere impostato facoltativamente su un heap descrittore per indicare che è associato a un elenco di comandi per riferimento dagli \_ \_ \_ \_ \_ shader. Gli heap dei  descrittori creati senza questo flag consentono alle applicazioni di impostare la fase dei descrittori nella memoria CPU prima di copiarli in un heap descrittore visibile allo shader, per praticità. Ma è anche bene che le applicazioni creino direttamente i descrittori negli heap dei descrittori visibili allo shader senza alcun requisito per la creazione di fasi nella CPU.

Questo flag si applica solo a CBV, SRV, UAV e campionatori. Non si applica ad altri tipi di heap del descrittore perché gli shader non fanno riferimento direttamente agli altri tipi.

Ad esempio, descrivere e creare un heap del descrittore del campionatore.


```C++
// Describe and create a sampler descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC samplerHeapDesc = {};
samplerHeapDesc.NumDescriptors = 1;
samplerHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER;
samplerHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&samplerHeapDesc, IID_PPV_ARGS(&m_samplerHeap)));
```



Descrivere e creare un heap dei descrittori di visualizzazione del buffer costante (CBV), visualizzazione risorse shader (SRV) e descrittore di visualizzazione di accesso non ordinato ( UAV).


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



## <a name="descriptor-handles"></a>Handle del descrittore

Le [**strutture D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) e [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) identificano descrittori specifici in un heap dei descrittori. Un handle è un po' come un puntatore, ma l'applicazione non deve dereferenziarlo manualmente. In caso contrario, il comportamento non è definito. L'uso degli handle deve passare attraverso l'API. Un handle stesso può essere copiato liberamente o passato in API che operano su/usano descrittori. Non esiste alcun conteggio dei riferimenti, pertanto l'applicazione deve assicurarsi che non usi un handle dopo l'eliminazione dell'heap del descrittore sottostante.

Le applicazioni possono individuare le dimensioni di incremento dei descrittori per un determinato tipo di heap descrittore, in modo che possano generare handle in qualsiasi posizione in un heap descrittore manualmente a partire dall'handle alla base. Le applicazioni non devono mai hardcoded come descrittore gestire le dimensioni di incremento e devono sempre eseguire query per una determinata istanza del dispositivo. In caso contrario, il comportamento non è definito. Le applicazioni non devono inoltre usare le dimensioni di incremento e gli handle per eseguire il proprio esame o manipolazione dei dati dell'heap dei descrittori, poiché i risultati di questa operazione non sono definiti. Gli handle non possono essere effettivamente usati come puntatori, ma come proxy per i puntatori in modo da evitare la dereferenziazione accidentale.

> [!Note]
>
> Esiste una struttura helper, CD3DX12 GPU DESCRIPTOR HANDLE, definita nell'intestazione \_ \_ \_ d3dx12.h, che eredita la struttura [**\_ \_ DESCRIPTOR \_ HANDLE della GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) e fornisce l'inizializzazione e altre operazioni utili. Analogamente, la struttura helper CD3DX12 CPU DESCRIPTOR HANDLE è definita per la struttura \_ \_ \_ [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)

 

Entrambe queste strutture helper vengono usate durante il popolamento degli elenchi di comandi.


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



## <a name="descriptor-heap-methods"></a>Metodi dell'heap dei descrittori

Gli heap dei descrittori ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) ereditano da [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable). Ciò impone la responsabilità della gestione della residenza degli heap dei descrittori nelle applicazioni, proprio come gli heap delle risorse. I metodi di gestione della residenza si applicano solo agli heap visibili dello shader perché gli heap non visibili allo shader non sono visibili direttamente alla GPU.

Il [**metodo ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) consente alle applicazioni di eseguire manualmente l'offset degli handle in un heap (producendo handle in qualsiasi punto in un heap descrittore). L'handle del percorso di avvio dell'heap deriva da [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) / [**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart). L'offset viene eseguito aggiungendo la dimensione di incremento del numero di descrittori da \* offset all'inizio dell'heap del descrittore. Si noti che la dimensione dell'incremento non può essere considerata come una dimensione in byte perché le applicazioni non devono dereferenziare gli handle come se fossero memoria. La memoria a cui punta ha un layout non standardizzato e può variare anche per un determinato dispositivo.

[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) restituisce un handle della CPU per gli heap dei descrittori visibili alla CPU. Restituisce un handle NULL (e il livello di debug segnala un errore) se l'heap del descrittore non è visibile alla CPU.

[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) restituisce un handle GPU per gli heap dei descrittori visibili allo shader. Restituisce un handle NULL (e il livello di debug segnala un errore) se l'heap del descrittore non è visibile allo shader.

Ad esempio, la creazione di visualizzazioni di destinazione di rendering per visualizzare il testo D2D usando un dispositivo 11on12.


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



## <a name="minimal-descriptor-heap-wrapper"></a>Wrapper heap del descrittore minimo

Gli sviluppatori di applicazioni probabilmente vorranno compilare il proprio codice helper per la gestione degli heap e degli handle del descrittore. Di seguito è riportato un esempio di base. Wrapper più sofisticati potrebbero, ad esempio, tenere traccia dei tipi di descrittori in cui si trova un heap e archiviare gli argomenti di creazione del descrittore.

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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap dei descrittori](descriptor-heaps.md)
</dt> </dl>

 

 