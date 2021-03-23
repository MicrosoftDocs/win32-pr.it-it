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
# <a name="creating-descriptor-heaps"></a>Creazione di heap descrittore

Per creare e configurare un heap del descrittore, è necessario selezionare un tipo di heap del descrittore, determinare il numero di descrittori in esso contenuti e impostare i flag che indicano se si tratta di una CPU visibile e/o uno shader visibile.

-   [Tipi di heap del descrittore](#descriptor-heap-types)
-   [Proprietà heap descrittore](#descriptor-heap-properties)
-   [Handle del descrittore](#descriptor-handles)
-   [Metodi dell'heap del descrittore](#descriptor-heap-methods)
-   [Wrapper dell'heap del descrittore minimo](#minimal-descriptor-heap-wrapper)
-   [Argomenti correlati](#related-topics)

## <a name="descriptor-heap-types"></a>Tipi di heap del descrittore

Il tipo di heap è determinato da un membro dell'enumerazione [**del \_ \_ \_ tipo di heap del descrittore D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) :

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

## <a name="descriptor-heap-properties"></a>Proprietà heap descrittore

Le proprietà dell'heap sono impostate sulla struttura [**\_ \_ \_ Desc del descrittore D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) , che fa riferimento sia alle enumerazioni del [**\_ \_ \_ tipo di heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) del descrittore di D3D12 sia alle enumerazioni dei [**\_ \_ \_ flag dell'heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)

Il flag dell' \_ heap del descrittore D3D12 del flag \_ \_ \_ \_ visibile può facoltativamente essere impostato in un heap del descrittore per indicare che è associato a un elenco di comandi per riferimento da shader. Gli heap del descrittore creati *senza* questo flag consentono alle applicazioni di organizzare i descrittori nella memoria della CPU prima di copiarli in un heap dei descrittori visibile dello shader, per praticità. Tuttavia, le applicazioni possono anche creare direttamente i descrittori negli heap dei descrittori visibili dello shader senza alcun requisito per la gestione temporanea di qualsiasi elemento sulla CPU.

Questo flag si applica solo a CBV, SRV, UAV e Samplers. Non si applica ad altri tipi di heap del descrittore perché gli shader non fanno direttamente riferimento ad altri tipi.

Ad esempio, descrivere e creare un heap del descrittore del campionatore.


```C++
// Describe and create a sampler descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC samplerHeapDesc = {};
samplerHeapDesc.NumDescriptors = 1;
samplerHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER;
samplerHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&samplerHeapDesc, IID_PPV_ARGS(&m_samplerHeap)));
```



Descrivere e creare una visualizzazione buffer costante (CBV), una visualizzazione risorse shader (SRV) e un heap descrittore UAV (unordered Access View).


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

Le strutture handle [**\_ \_ descrittore \_ GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) e [**\_ \_ descrittore \_ CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) identificano descrittori specifici in un heap del descrittore. Un handle è un bit come un puntatore, ma l'applicazione non deve dereferenziarla manualmente; in caso contrario, il comportamento non è definito. L'uso degli handle deve passare attraverso l'API. Un handle può essere copiato liberamente o passato in API che operano in/usano i descrittori. Non esiste un conteggio dei riferimenti, quindi l'applicazione deve assicurarsi che non usi un handle dopo l'eliminazione dell'heap del descrittore sottostante.

Le applicazioni possono individuare le dimensioni di incremento dei descrittori per un determinato tipo di heap del descrittore, in modo da poter generare manualmente gli handle in qualsiasi posizione in un heap del descrittore a partire dall'handle alla base. Le applicazioni non devono mai impostare come hardcoded le dimensioni di incremento dell'handle del descrittore e devono sempre eseguire una query per una determinata istanza del dispositivo. in caso contrario, il comportamento non è definito. Le applicazioni non devono inoltre utilizzare le dimensioni e gli handle di incremento per eseguire i propri esami o la manipolazione dei dati dell'heap del descrittore, perché i risultati di tale operazione non sono definiti. Gli handle possono non essere effettivamente usati come puntatori, bensì come proxy per i puntatori in modo da evitare la dereferenziazione accidentale.

> [!Note]
>
> È presente una struttura di supporto, \_ \_ handle descrittore GPU CD3DX12 \_ , definita nell'intestazione d3dx12. h, che eredita la struttura dell' [**\_ \_ \_ handle del descrittore della GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) e fornisce l'inizializzazione e altre operazioni utili. Analogamente \_ , la \_ struttura di supporto del descrittore della CPU CD3DX12 \_ è definita per la struttura dell' [**\_ \_ \_ handle descrittore della CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .

 

Entrambe le strutture helper vengono utilizzate durante la compilazione degli elenchi di comandi.


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



## <a name="descriptor-heap-methods"></a>Metodi dell'heap del descrittore

Gli heap dei descrittori ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) ereditano da [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable). Ciò impone la responsabilità della gestione della residenza degli heap del descrittore nelle applicazioni, proprio come gli heap delle risorse. I metodi di gestione della residenza si applicano solo agli heap visibili dello shader poiché gli heap visibili non shader non sono visibili direttamente alla GPU.

Il metodo [**ID3D12Device:: GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) consente alle applicazioni di eseguire manualmente l'offset degli handle in un heap (generando handle in un punto qualsiasi in un heap del descrittore). Il punto di controllo dell'inizio dell'heap deriva da [**ID3D12DescriptorHeap:: GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) / [**ID3D12DescriptorHeap:: GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart). La compensazione viene eseguita aggiungendo le dimensioni di incremento \* del numero di descrittori da compensare all'inizio dell'heap del descrittore. Si noti che la dimensione di incremento non può essere considerata come una dimensione in byte poiché le applicazioni non devono dereferenziare gli handle come se fossero memoria: la memoria a cui puntava ha un layout non standardizzato e può variare anche per un determinato dispositivo.

[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) restituisce un handle CPU per gli heap del descrittore visibile della CPU. Restituisce un handle NULL (e il livello di debug segnalerà un errore) se l'heap del descrittore non è visibile alla CPU.

[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) restituisce un handle GPU per gli heap del descrittore visibile dello shader. Restituisce un handle NULL (e il livello di debug segnalerà un errore) se l'heap del descrittore non è visibile.

Ad esempio, creazione di visualizzazioni di destinazione di rendering per visualizzare il testo D2D usando un dispositivo 11on12.


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



## <a name="minimal-descriptor-heap-wrapper"></a>Wrapper dell'heap del descrittore minimo

È probabile che gli sviluppatori di applicazioni desiderino compilare il proprio codice di supporto per la gestione degli heap e degli handle del descrittore. Di seguito è riportato un esempio di base. I wrapper più sofisticati potrebbero, ad esempio, tenere traccia dei tipi di descrittori che si trovano in un heap e archiviano gli argomenti di creazione del descrittore.

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

[Heap descrittore](descriptor-heaps.md)
</dt> </dl>

 

 