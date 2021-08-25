---
title: Creazione e registrazione di elenchi di comandi e bundle
description: Questo argomento descrive la registrazione di elenchi di comandi e bundle nelle app Direct3D 12. Sia gli elenchi di comandi che i bundle consentono alle app di registrare chiamate di disegno o di modifica dello stato per un'esecuzione successiva nell'unità di elaborazione grafica (GPU).
ms.assetid: 0074B796-33A4-4AA1-A4E7-48A2A63F25B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480819cbd421b30cbf54a58578c02056d37d7e36bf2ead845c19e438df54cbb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850713"
---
# <a name="creating-and-recording-command-lists-and-bundles"></a>Creazione e registrazione di elenchi di comandi e bundle

Questo argomento descrive la registrazione di elenchi di comandi e bundle nelle app Direct3D 12. Sia gli elenchi di comandi che i bundle consentono alle app di registrare chiamate di disegno o di modifica dello stato per un'esecuzione successiva nell'unità di elaborazione grafica (GPU).

Oltre agli elenchi di comandi, l'API sfrutta la funzionalità presente nell'hardware GPU aggiungendo un secondo livello di elenchi di comandi, denominati *bundle*. Lo scopo dei bundle è consentire alle app di raggruppare un numero ridotto di comandi API per un'esecuzione successiva. Al momento della creazione del bundle, il driver eseguirà il maggior numero possibile di operazioni di pre-elaborazione per renderle convenienti per l'esecuzione in un secondo momento. I bundle sono progettati per essere usati e ri-usati per un numero qualsiasi di volte. Gli elenchi di comandi, d'altra parte, vengono in genere eseguiti solo una volta. Tuttavia, un *elenco* di comandi può essere eseguito più volte,purché l'applicazione garantisca che le esecuzioni precedenti siano state completate prima di inviare nuove esecuzioni.

In genere, tuttavia, la compilazione di chiamate API in bundle, chiamate API e aggregazioni in elenchi di comandi ed elenchi di comandi in un singolo frame, è illustrata nel diagramma seguente, notando il riutilizzo del **Bundle 1** nell'elenco comandi **1** e nell'elenco comandi **2** e che i nomi dei metodi API nel diagramma sono come esempi, è possibile usare molte chiamate API diverse.

![compilazione di comandi, aggregazioni ed elenchi di comandi in frame](images/gpu-workitems.png)

Esistono diverse restrizioni per la creazione e l'esecuzione di aggregazioni ed elenchi di comandi diretti e queste differenze vengono notate in questo argomento.

## <a name="creating-command-lists"></a>Creazione di elenchi di comandi

Gli elenchi di comandi diretti e i bundle vengono creati chiamando [**ID3D12Device::CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) [**o ID3D12Device4::CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1).

Usare [**ID3D12Device4::CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1) per creare un elenco di comandi chiuso, anziché creare un nuovo elenco e chiuderlo immediatamente. In questo modo si evita l'inefficienza di creare un elenco con un allocatore e pso, ma non usarli.

[**ID3D12Device::CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) accetta i parametri seguenti come input:

### <a name="d3d12_command_list_type"></a>TIPO DI ELENCO COMANDI D3D12 \_ \_ \_

[**L'enumerazione D3D12 \_ COMMAND LIST \_ \_ TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) indica il tipo di elenco di comandi che viene creato. Può essere un elenco di comandi diretto, un bundle, un elenco di comandi di calcolo o un elenco di comandi di copia.

### <a name="id3d12commandallocator"></a>ID3D12CommandAllocator

Un allocatore di comandi consente all'app di gestire la memoria allocata per gli elenchi di comandi. L'allocatore di comandi viene creato chiamando [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator). Quando si crea un elenco di comandi, il tipo di elenco di comandi dell'allocatore, specificato da [**D3D12 \_ COMMAND \_ LIST \_ TYPE,**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)deve corrispondere al tipo di elenco di comandi creato. Un allocatore specificato può essere  associato a non più di un elenco di comandi attualmente registrato alla volta, anche se un allocatore di comandi può essere usato per creare un numero qualsiasi di [**oggetti GraphicsCommandList.**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)

Per recuperare la memoria allocata da un allocatore di comandi, un'app chiama [**ID3D12CommandAllocator::Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset). In questo modo l'allocatore può essere riutilizzato per i nuovi commmand, ma non ridurrà le dimensioni sottostanti. Prima di eseguire questa operazione, tuttavia, l'app deve assicurarsi che la GPU non eserciti più elenchi di comandi associati all'allocatore. In caso contrario, la chiamata avrà esito negativo. Si noti inoltre che questa API non è a thread libero e pertanto non può essere chiamata nello stesso allocatore contemporaneamente da più thread.

### <a name="id3d12pipelinestate"></a>ID3D12PipelineState

Stato iniziale della pipeline per l'elenco di comandi. In Microsoft Direct3D 12 la maggior parte dello stato della pipeline grafica viene impostata all'interno di un elenco di comandi usando [**l'oggetto ID3D12PipelineState.**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) Un'app ne creerà un numero elevato, in genere durante l'inizializzazione dell'app, e quindi lo stato viene aggiornato modificando l'oggetto stato attualmente associato usando [**ID3D12GraphicsCommandList::SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate). Per altre informazioni sugli oggetti stato della pipeline, vedere [Gestione dello stato della pipeline grafica in Direct3D 12.](managing-graphics-pipeline-state-in-direct3d-12.md)

Si noti che i bundle non ereditano lo stato della pipeline impostato dalle chiamate precedenti negli elenchi di comandi diretti che sono i relativi elementi padre.

Se questo parametro è NULL, viene usato uno stato predefinito.

## <a name="recording-command-lists"></a>Registrazione di elenchi di comandi

Subito dopo la creazione, gli elenchi di comandi sono nello stato di registrazione. È anche possibile usare di nuovo un elenco di comandi esistente chiamando I [**D3D12GraphicsCommandList::Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset), che lascia anche l'elenco di comandi nello stato di registrazione. A [**differenza di ID3D12CommandAllocator::Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset), è possibile chiamare **Reset** mentre l'elenco di comandi è ancora in esecuzione. Un modello tipico è inviare un elenco di comandi e quindi reimpostarlo immediatamente per riutilizzare la memoria allocata per un altro elenco di comandi. Si noti che un solo elenco di comandi associato a ogni allocatore di comandi può essere in uno stato di registrazione contemporaneamente.

Quando un elenco di comandi è nello stato di registrazione, è sufficiente chiamare i metodi [**dell'interfaccia ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) per aggiungere comandi all'elenco. Molti di questi metodi consentono funzionalità Direct3D comuni che saranno familiari agli sviluppatori Microsoft Direct3D 11; altre API sono nuove per Direct3D 12.

Dopo aver aggiunto comandi all'elenco di comandi, è possibile eseguire la transizione dell'elenco di comandi dallo stato di registrazione chiamando [**Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).

Gli allocatori dei comandi possono aumentare ma non ridursi. È consigliabile considerare gli allocatori di pool e riutilizzo per ottimizzare l'efficienza dell'app. È possibile registrare più elenchi nello stesso allocatore prima della reimpostazione, purché venga registrato un solo elenco per un determinato allocatore contemporaneamente. È possibile visualizzare ogni elenco come proprietario di una parte dell'allocatore che indica quale [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) verrà eseguito.

Una strategia di pooling di allocatori semplice deve mirare a circa `numCommandLists * MaxFrameLatency` gli allocatori. Ad esempio, se si registrano 6 elenchi e si consentono fino a 3 frame latenti, è ragionevolmente possibile prevedere 18-20 allocatori. Una strategia di pooling più avanzata, che riutilizza gli allocatori per più elenchi nello stesso thread, potrebbe puntare ad `numRecordingThreads * MaxFrameLatency` allocatori. Usando l'esempio precedente, se 2 elenchi sono stati registrati sul thread A, 2 sul thread B, 1 sul thread C e 1 sul thread D, è possibile mirare realisticamente a 12-14 allocatori.

Usare un limite per determinare quando un allocatore specificato può essere riutilizzato.

Poiché gli elenchi di comandi possono essere reimpostati immediatamente dopo l'esecuzione, possono essere in pool semplice, aggiungendoli di nuovo al pool dopo ogni chiamata a [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

## <a name="example"></a>Esempio

I frammenti di codice seguenti illustrano la creazione e la registrazione di un elenco di comandi. Si noti che questo esempio include le funzionalità direct3D 12 seguenti:

-   Oggetti di stato della pipeline: vengono usati per impostare la maggior parte dei parametri di stato della pipeline di rendering dall'interno di un elenco di comandi. Per altre informazioni, vedere [Gestione dello stato della pipeline grafica in Direct3D 12.](managing-graphics-pipeline-state-in-direct3d-12.md)
-   Heap descrittore: le app usano heap descrittori per gestire l'associazione della pipeline alle risorse di memoria.
-   Barriera delle risorse: viene usata per gestire la transizione delle risorse da uno stato a un altro, ad esempio da una visualizzazione di destinazione di rendering a una visualizzazione delle risorse shader. Per altre informazioni, vedere [Uso delle barriere alle risorse per sincronizzare gli stati delle risorse.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

Ad esempio,


```C++
void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr<ID3DBlob> vertexShader;
        ComPtr<ID3DBlob> pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast<UINT8*>(vertexShader->GetBufferPointer()), vertexShader->GetBufferSize() };
        psoDesc.PS = { reinterpret_cast<UINT8*>(pixelShader->GetBufferPointer()), pixelShader->GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList->Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer->Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device->CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
```



Dopo che un elenco di comandi è stato creato e registrato, può essere eseguito usando una coda di comandi. Per altre informazioni, vedere [Esecuzione e sincronizzazione degli elenchi di comandi](executing-and-synchronizing-command-lists.md).

## <a name="reference-counting"></a>Conteggio riferimenti

La maggior parte delle API D3D12 continua a usare il conteggio dei riferimenti nelle convenzioni COM seguenti. Un'eccezione importante è l'API dell'elenco di comandi di grafica D3D12. Tutte le API in [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) non contengono riferimenti agli oggetti passati a tali API. Ciò significa che le applicazioni sono responsabili di garantire che un elenco di comandi non sia mai inviato per l'esecuzione che fa riferimento a una risorsa distrutta.

## <a name="command-list-errors"></a>Errori dell'elenco comandi

La maggior parte delle API in [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) non restituisce errori. Gli errori rilevati durante la creazione dell'elenco di comandi vengono posticimanti fino a [**ID3D12GraphicsCommandList::Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close). L'unica eccezione è DXGI \_ ERROR \_ DEVICE \_ REMOVED, che viene rinviata ulteriormente. Si noti che questa operazione è diversa da D3D11, in cui molti errori di convalida dei parametri vengono eliminati automaticamente e non vengono mai restituiti al chiamante.

Le applicazioni possono prevedere errori DXGI \_ DEVICE REMOVED nelle chiamate API \_ seguenti:

-   Qualsiasi metodo di creazione di risorse
-   [**ID3D12Resource::Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)
-   [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**GetDeviceRemovedReason**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)

## <a name="command-list-api-restrictions"></a>Restrizioni dell'API dell'elenco di comandi

Alcune API dell'elenco di comandi possono essere chiamate solo in determinati tipi di elenchi di comandi. La tabella seguente mostra quali API dell'elenco di comandi sono valide per chiamare su ogni tipo di elenco di comandi. Mostra anche quali API sono valide per chiamare in un passaggio di [**rendering D3D12.**](./direct3d-12-render-passes.md) 

| Nome API                                         | Grafica | Calcolo | Copia | Bundle | In passaggio di rendering |
|--------------------------------------------------|:--------:|:-------:|:----:|:------:|:--------------:|
| AtomicCopyBufferUINT                             | ✓        | ✓       | ✓    |        |                |
| AtomicCopyBufferUINT64                           | ✓        | ✓       | ✓    |        |                |
| BeginQuery                                       | ✓        |         |      |        | ✓              |
| BeginRenderPass                                  | ✓        |         |      |        |                |
| BuildRaytracingAccelerationStructure             | ✓        | ✓       |      |        |                |
| ClearDepthStencilView                            | ✓        |         |      |        |                |
| ClearRenderTargetView                            | ✓        |         |      |        |                |
| ClearState                                       | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewFloat                    | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewUint                     | ✓        | ✓       |      |        |                |
| CopyBufferRegion                                 | ✓        | ✓       | ✓    |        |                |
| CopyRaytracingAccelerationStructure              | ✓        | ✓       |      |        |                |
| CopyResource                                     | ✓        | ✓       | ✓    |        |                |
| CopyTextureRegion                                | ✓        | ✓       | ✓    |        |                |
| CopyTiles                                        | ✓        | ✓       | ✓    |        |                |
| DiscardResource                                  | ✓        | ✓       |      |        |                |
| Dispatch                                         | ✓        | ✓       |      | ✓      |                |
| DispatchRays                                     | ✓        | ✓       |      | ✓      |                |
| DrawIndexedInstanced                             | ✓        |         |      | ✓      | ✓              |
| DrawInstanced                                    | ✓        |         |      | ✓      | ✓              |
| EmitRaytracingAccelerationStructurePostbuildInfo | ✓        | ✓       |      |        |                |
| EndQuery                                         | ✓        | ✓       | ✓    |        | ✓              |
| EndRenderPass                                    | ✓        |         |      |        | ✓              |
| ExecuteBundle                                    | ✓        |         |      |        | ✓              |
| ExecuteIndirect                                  | ✓        | ✓       |      | ✓      | ✓              |
| ExecuteMetaCommand                               | ✓        | ✓       |      |        |                |
| IASetIndexBuffer                                 | ✓        |         |      | ✓      | ✓              |
| IASetPrimitiveTopology                           | ✓        |         |      | ✓      | ✓              |
| IASetVertexBuffers                               | ✓        |         |      | ✓      | ✓              |
| InitializeMetaCommand                            | ✓        | ✓       |      |        |                |
| OMSetBlendFactor                                 | ✓        |         |      | ✓      | ✓              |
| OMSetDepthBounds                                 | ✓        |         |      | ✓      | ✓              |
| OMSetRenderTargets                               | ✓        |         |      |        |                |
| OMSetStencilRef                                  | ✓        |         |      | ✓      | ✓              |
| ResolveQueryData                                 | ✓        | ✓       | ✓    |        |                |
| ResolveSubresource                               | ✓        |         |      |        |                |
| ResolveSubresourceRegion                         | ✓        |         |      |        |                |
| ResourceBarrier                                  | ✓        | ✓       | ✓    |        | ✓              |
| RSSetScissorRects                                | ✓        |         |      |        | ✓              |
| RSSetShadingRate                                 | ✓        |         |      | ✓      | ✓              |
| RSSetShadingRateImage                            | ✓        |         |      | ✓      | ✓              |
| RSSetViewports                                   | ✓        |         |      |        | ✓              |
| SetComputeRoot32BitConstant                      | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRoot32BitConstants                     | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootConstantBufferView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootDescriptorTable                    | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootShaderResourceView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootSignature                          | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootUnorderedAccessView                | ✓        | ✓       |      | ✓      | ✓              |
| SetDescriptorHeaps                               | ✓        | ✓       |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstant                     | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstants                    | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootConstantBufferView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootDescriptorTable                   | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootShaderResourceView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootSignature                         | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootUnorderedAccessView               | ✓        |         |      | ✓      | ✓              |
| SetPipelineState                                 | ✓        | ✓       |      | ✓      | ✓              |
| SetPipelineState1                                | ✓        | ✓       |      | ✓      |                |
| SetPredication                                   | ✓        | ✓       |      |        | ✓              |
| SetProtectedResourceSession                      | ✓        | ✓       | ✓    |        |                |
| SetSamplePositions                               | ✓        |         |      | ✓      | ✓              |
| SetViewInstanceMask                              | ✓        |         |      | ✓      | ✓              |
| SOSetTargets                                     | ✓        |         |      |        | ✓              |
| WriteBufferImmediate                             | ✓        | ✓       | ✓    | ✓      | ✓              |

## <a name="bundle-restrictions"></a>Restrizioni dell'aggregazione

Le restrizioni consentono ai driver Direct3D 12 di eseguire la maggior parte del lavoro associato ai bundle in fase di registrazione, consentendo l'esecuzione dell'API [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) con un sovraccarico ridotto. Tutti gli oggetti stato della pipeline a cui fa riferimento un bundle devono avere gli stessi formati di destinazione di rendering, il formato del buffer di profondità e le descrizioni di esempio.

Le chiamate API dell'elenco di comandi seguenti non sono consentite per gli elenchi di comandi creati con tipo: D3D12 \_ COMMAND \_ LIST TYPE \_ \_ BUNDLE:

-   Qualsiasi metodo Clear
-   Qualsiasi metodo Copy
-   [**DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
-   [**ResolveSubresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**SetPredication**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)
-   [**BeginQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
-   [**EndQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
-   [**SOSetTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)
-   [**OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
-   [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)
-   [**RSSetScissorRects**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)

[**È possibile chiamare SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) in un bundle, ma gli heap dei descrittori del bundle devono corrispondere all'heap dei descrittori dell'elenco dei comandi chiamanti.

Se una di queste API viene chiamata in un bundle, il runtime elimina la chiamata. Il livello di debug genererà un errore ogni volta che si verifica questa situazione.

## <a name="related-topics"></a>Argomenti correlati

[Invio di lavoro in Direct3D 12](command-queues-and-command-lists.md)