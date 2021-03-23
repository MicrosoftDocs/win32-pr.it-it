---
title: Creazione e registrazione di elenchi di comandi e bundle
description: Questo argomento descrive la registrazione di elenchi di comandi e bundle nelle app Direct3D 12. Gli elenchi di comandi e i bundle consentono alle app di registrare le chiamate di disegno o modifica dello stato per un'esecuzione successiva sull'unità di elaborazione grafica (GPU).
ms.assetid: 0074B796-33A4-4AA1-A4E7-48A2A63F25B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ef2b54138cf3a08b85e3e8cc31f97cbe66abf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548859"
---
# <a name="creating-and-recording-command-lists-and-bundles"></a>Creazione e registrazione di elenchi di comandi e bundle

Questo argomento descrive la registrazione di elenchi di comandi e bundle nelle app Direct3D 12. Gli elenchi di comandi e i bundle consentono alle app di registrare le chiamate di disegno o modifica dello stato per un'esecuzione successiva sull'unità di elaborazione grafica (GPU).

Oltre agli elenchi di comandi, l'API sfrutta le funzionalità presenti nell'hardware GPU aggiungendo un secondo livello di elenchi di comandi, detti *bundle*. Lo scopo dei bundle è consentire alle app di raggruppare un numero ridotto di comandi API per un'esecuzione successiva. Al momento della creazione del bundle, il driver eseguirà la maggior parte delle operazioni di pre-elaborazione, in quanto è possibile renderle più convenienti da eseguire in un secondo momento. I bundle sono progettati per essere usati e riutilizzati un numero qualsiasi di volte. Gli elenchi di comandi, invece, vengono in genere eseguiti solo una volta sola. Tuttavia, un elenco di comandi *può* essere eseguito più volte (purché l'applicazione assicuri che le esecuzioni precedenti siano state completate prima di inviare nuove esecuzioni).

In genere, tuttavia, la compilazione di chiamate API in bundle e chiamate API e aggregazioni in elenchi di comandi ed elenchi di comandi in un unico frame, viene illustrato nel diagramma seguente, annotando il riutilizzo del **Bundle 1** nell'**elenco** dei comandi 1 e nell' **elenco di comandi 2** e che i nomi dei metodi API nel diagramma sono come esempi, è possibile utilizzare molte chiamate API.

![compilazione di comandi, bundle ed elenchi di comandi in frame](images/gpu-workitems.png)

Esistono diverse restrizioni per la creazione e l'esecuzione di bundle ed elenchi di comandi diretti e queste differenze sono indicate in questo argomento.

## <a name="creating-command-lists"></a>Creazione di elenchi di comandi

Gli elenchi di comandi diretti e i bundle vengono creati chiamando [**ID3D12Device:: CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) o [**ID3D12Device4:: CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1).

Usare [**ID3D12Device4:: CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1) per creare un elenco di comandi chiuso, anziché creare un nuovo elenco e chiuderlo immediatamente. In questo modo si evita l'inefficienza della creazione di un elenco con un allocatore e un oggetto PSO senza utilizzarli.

[**ID3D12Device:: CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) accetta come input i parametri seguenti:

### <a name="d3d12_command_list_type"></a>\_Tipo di \_ elenco di comandi D3D12 \_

L'enumerazione del [**\_ tipo di \_ elenco \_ dei comandi D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) indica il tipo di elenco di comandi da creare. Può trattarsi di un elenco di comandi diretto, un bundle, un elenco di comandi di calcolo o un elenco di comandi di copia.

### <a name="id3d12commandallocator"></a>ID3D12CommandAllocator

Un allocatore di comandi consente all'app di gestire la memoria allocata per gli elenchi di comandi. L'allocatore di comandi viene creato chiamando [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator). Quando si crea un elenco di comandi, il tipo di elenco dei comandi dell'allocatore, specificato dal [**\_ \_ \_ tipo di elenco**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)dei comandi D3D12, deve corrispondere al tipo di elenco di comandi da creare. Un allocatore specificato può essere associato a non più di un elenco di comandi attualmente in fase di *registrazione* , ma è possibile usare un allocatore di comandi per creare un numero qualsiasi di oggetti [**GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) .

Per recuperare la memoria allocata da un allocatore di comandi, un'app chiama [**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset). Ciò consente di riutilizzare l'allocatore per i nuovi commmands, ma non di ridurne le dimensioni sottostanti. Tuttavia, prima di eseguire questa operazione, l'app deve assicurarsi che la GPU non esegua più elenchi di comandi associati all'allocatore; in caso contrario, la chiamata avrà esito negativo. Si noti inoltre che questa API non è a thread libero e pertanto non può essere chiamata sullo stesso allocatore nello stesso momento da più thread.

### <a name="id3d12pipelinestate"></a>ID3D12PipelineState

Stato iniziale della pipeline per l'elenco dei comandi. In Microsoft Direct3D 12 la maggior parte dello stato della pipeline grafica viene impostata in un elenco di comandi utilizzando l'oggetto [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) . Un'app creerà un numero elevato di questi, in genere durante l'inizializzazione dell'app e lo stato viene aggiornato cambiando l'oggetto stato attualmente associato usando [**ID3D12GraphicsCommandList:: SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate). Per ulteriori informazioni sugli oggetti stato della pipeline, vedere [gestione dello stato della pipeline grafica in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

Si noti che i bundle non ereditano lo stato della pipeline impostato dalle chiamate precedenti negli elenchi di comandi diretti che sono elementi padre.

Se questo parametro è NULL, viene utilizzato uno stato predefinito.

## <a name="recording-command-lists"></a>Registrazione degli elenchi di comandi

Subito dopo la creazione, gli elenchi di comandi si trovano nello stato di registrazione. È anche possibile riusare un elenco di comandi esistente chiamando [**D3D12GraphicsCommandList:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset), che lascia anche l'elenco dei comandi nello stato di registrazione. A differenza di [**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset), è possibile chiamare **Reset** mentre è ancora in corso l'esecuzione dell'elenco dei comandi. Un modello tipico consiste nell'inviare un elenco di comandi e quindi reimpostarlo immediatamente per riutilizzare la memoria allocata per un altro elenco di comandi. Si noti che solo un elenco di comandi associato a ogni allocatore di comandi può essere in uno stato di registrazione alla volta.

Quando un elenco di comandi è nello stato di registrazione, è sufficiente chiamare i metodi dell'interfaccia [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) per aggiungere comandi all'elenco. Molti di questi metodi consentono funzionalità comuni di Direct3D che saranno note agli sviluppatori Microsoft Direct3D 11; altre API sono nuove per Direct3D 12.

Dopo aver aggiunto i comandi all'elenco dei comandi, è possibile eseguire la transizione dell'elenco di comandi fuori dallo stato di registrazione chiamando [**Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).

Gli allocatori di comandi possono crescere ma non compattare e riutilizzare gli allocatori devono essere presi in considerazione per ottimizzare l'efficienza dell'app. È possibile registrare più elenchi nello stesso allocatore prima che venga reimpostato, purché un solo elenco venga registrato in un determinato allocatore alla volta. È possibile visualizzare ogni elenco come proprietario di una parte dell'allocatore, che indica che [**ID3D12CommandQueue:: oggetti executecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) verrà eseguito.

Una semplice strategia di pool allocatori deve puntare a circa gli `numCommandLists * MaxFrameLatency` allocatori. Se, ad esempio, si registrano 6 elenchi e si concedono fino a 3 frame latenti, si potrebbero ragionevolmente prevedere 18-20 allocatori. Una strategia di pooling più avanzata, che riutilizza gli allocatori per più elenchi sullo stesso thread, potrebbe puntare agli `numRecordingThreads * MaxFrameLatency` allocatori. Utilizzando l'esempio precedente, se due elenchi sono stati registrati nel thread A, 2 sul thread B, 1 sul thread C e 1 sul thread D, è possibile puntare in maniera realistica agli allocatori 12-14.

Utilizzare una recinzione per determinare quando è possibile riutilizzare un allocatore specificato.

Poiché gli elenchi di comandi possono essere reimpostati immediatamente dopo l'esecuzione, possono essere raggruppati in modo banale, aggiungendoli nuovamente al pool dopo ogni chiamata a [**ID3D12CommandQueue:: oggetti executecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

## <a name="example"></a>Esempio

I frammenti di codice seguenti illustrano la creazione e la registrazione di un elenco di comandi. Si noti che questo esempio include le funzionalità di Direct3D 12 seguenti:

-   Oggetti stato della pipeline: vengono usati per impostare la maggior parte dei parametri di stato della pipeline di rendering dall'interno di un elenco di comandi. Per altre informazioni, vedere [gestione dello stato della pipeline grafica in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).
-   Heap descrittore: le app usano gli heap descrittore per gestire l'associazione della pipeline alle risorse di memoria.
-   Barriera delle risorse: viene usato per gestire la transizione delle risorse da uno stato a un altro, ad esempio da una visualizzazione della destinazione di rendering a una visualizzazione risorse dello shader. Per ulteriori informazioni, vedere [utilizzo delle barriere delle risorse per sincronizzare gli Stati delle risorse](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

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



Una volta creato e registrato un elenco di comandi, è possibile eseguirlo utilizzando una coda di comandi. Per ulteriori informazioni, vedere [esecuzione e sincronizzazione degli elenchi di comandi](executing-and-synchronizing-command-lists.md).

## <a name="reference-counting"></a>Conteggio riferimenti

La maggior parte delle API D3D12 continua a usare il conteggio dei riferimenti dopo le convenzioni COM. Un'eccezione notevole è rappresentata dalle API dell'elenco dei comandi di D3D12 graphics. Tutte le API in [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) non contengono riferimenti agli oggetti passati a tali API. Ciò significa che le applicazioni sono responsabili di garantire che un elenco di comandi non venga mai inviato per l'esecuzione che fa riferimento a una risorsa distrutta.

## <a name="command-list-errors"></a>Errori elenco comandi

La maggior parte delle API in [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) non restituisce errori. Gli errori rilevati durante la creazione dell'elenco di comandi vengono posticipati fino a [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close). L'unica eccezione è il \_ dispositivo DXGI Error \_ \_ rimosso, che viene rinviato ancora più a fondo. Si noti che questo è diverso da D3D11, dove molti errori di convalida dei parametri vengono eliminati automaticamente e non vengono mai restituiti al chiamante.

Le applicazioni possono prevedere che \_ i dispositivi DXGI \_ rimossi gli errori nelle chiamate API seguenti:

-   Qualsiasi metodo di creazione di risorse
-   [**ID3D12Resource:: Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)
-   [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**GetDeviceRemovedReason**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)

## <a name="command-list-api-restrictions"></a>Restrizioni API dell'elenco comandi

Alcune API dell'elenco di comandi possono essere chiamate solo su determinati tipi di elenchi di comandi. Nella tabella seguente vengono illustrate le API dell'elenco di comandi valide per la chiamata a ogni tipo di elenco di comandi. Mostra anche quali API sono valide per chiamare in un [**passaggio di rendering D3D12**](./direct3d-12-render-passes.md). 

| Nome API                                         | Grafica | Calcolo | Copia | Bundle | Nel passaggio di rendering |
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

## <a name="bundle-restrictions"></a>Restrizioni del bundle

Le restrizioni consentono ai driver Direct3D 12 di eseguire la maggior parte del lavoro associato ai bundle in fase di registrazione, consentendo così l'esecuzione dell'API [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) con un sovraccarico ridotto. Tutti gli oggetti di stato della pipeline a cui fa riferimento un bundle devono avere gli stessi formati di destinazione di rendering, il formato del buffer di profondità e le descrizioni di esempio.

Le chiamate API dell'elenco di comandi seguenti non sono consentite negli elenchi di comandi creati con il tipo di \_ elenco dei comandi D3D12 \_ \_ \_ :

-   Qualsiasi metodo Clear
-   Qualsiasi metodo di copia
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

[**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) può essere chiamato su un bundle, ma gli heap del descrittore del bundle devono corrispondere all'heap del descrittore dell'elenco dei comandi chiamante.

Se una di queste API viene chiamata su un bundle, la chiamata verrà eliminata dal runtime. Il livello di debug genererà un errore ogni volta che si verifica questo problema.

## <a name="related-topics"></a>Argomenti correlati

[Invio di lavoro in Direct3D 12](command-queues-and-command-lists.md)