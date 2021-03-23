---
title: Creazione di un componente Direct3D 12 di base
description: In questo argomento viene descritto il flusso di chiamate per creare un componente Direct3D 12 di base.
ms.assetid: A0FB108B-15C1-42AD-9277-D5CB63FA8329
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: d0c7ead9ce67ee23a0668304a006d6cd67fb3d67
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "104758861"
---
# <a name="creating-a-basic-direct3d-12-component"></a>Creazione di un componente Direct3D 12 di base

> [!NOTE]
> Vedere il repository [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) per gli esempi di grafica DirectX 12 che illustrano come creare applicazioni con utilizzo intensivo di grafica per Windows 10.

In questo argomento viene descritto il flusso di chiamate per creare un componente Direct3D 12 di base.

-   [Flusso di codice per un'app semplice](#code-flow-for-a-simple-app)
    -   [Inizializzare](#initialize)
    -   [Aggiornamento](#update)
    -   [Rendering](#render)
    -   [Eliminare](#destroy)
-   [Esempio di codice per un'app semplice](#code-example-for-a-simple-app)
    -   [Classe D3D12HelloTriangle](#class-d3d12hellotriangle)
    -   [OnInit ()](#oninit)
    -   [LoadPipeline()](#loadpipeline)
    -   [LoadAssets()](#loadassets)
    -   [OnUpdate ()](#onupdate)
    -   [OnRender ()](#onrender)
    -   [PopulateCommandList()](#populatecommandlist)
    -   [WaitForPreviousFrame()](#waitforpreviousframe)
    -   [OnDestroy ()](#ondestroy)
-   [Argomenti correlati](#related-topics)

## <a name="code-flow-for-a-simple-app"></a>Flusso di codice per un'app semplice

Il ciclo più esterno di un programma D3D 12 segue un processo grafico molto standard:

> [!TIP]
> Le nuove funzionalità di Direct3D 12 sono seguite da una nota.

-   [Inizializzare](#initialize)
-   **Ripetere**
    -   [Aggiornamento](#update)
    -   [Rendering](#render)
-   [Eliminare](#destroy)

### <a name="initialize"></a>Inizializzare

L'inizializzazione prevede innanzitutto la configurazione delle variabili e delle classi globali, mentre una funzione Initialize deve preparare la pipeline e gli asset.

-   Inizializzare la pipeline.
    -   Abilitare il livello debug.
    -   Creare il dispositivo.
    -   Creare la coda dei comandi.
    -   Creare la catena di scambio.
    -   Creare un heap del descrittore RTV (render target View).
        > [!Note]  
        > Un [heap del descrittore](descriptor-heaps.md) può essere considerato come una matrice di [descrittori](descriptors.md). Dove ogni descrittore descrive completamente un oggetto alla GPU.

    -   Creare risorse frame (visualizzazione della destinazione di rendering per ogni frame).
    -   Creare un allocatore di comandi.
        > [!Note]  
        > Un allocatore di comandi gestisce l'archiviazione sottostante per gli [elenchi di comandi e i bundle](recording-command-lists-and-bundles.md).
         
-   Inizializzare gli asset.
    -   Crea una firma radice vuota.
        > [!Note]  
        > Una [firma radice](root-signatures.md) grafica definisce quali risorse sono associate alla pipeline grafica.

    -   Compilare gli shader.
    -   Creare il layout di input vertice.
    -   Creare una descrizione dell' [oggetto stato della pipeline](managing-graphics-pipeline-state-in-direct3d-12.md) , quindi creare l'oggetto.
        > [!Note]  
        > Un oggetto di stato della pipeline gestisce lo stato di tutti gli shader attualmente impostati, nonché alcuni oggetti di stato della funzione fissa, ad esempio l' *assembler di input*, *Tesselator*, *rasterizzatore* e *Unione di output*.

    -   Creare l'elenco dei comandi.
    -   Chiudere l'elenco dei comandi.
    -   Creare e caricare i buffer dei vertici.
    -   Creare le visualizzazioni del buffer dei vertici.
    -   Creare una recinzione.
        > [!Note]  
        > Viene usata una recinzione per sincronizzare la CPU con la GPU (vedere [sincronizzazione multimotore](./user-mode-heap-synchronization.md)).

    -   Creare un handle di evento.
    -   Attendere il completamento della GPU.
        > [!Note]  
        > Controllare la barriera.

Vedere la [classe D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [LoadPipeline](#loadpipeline) e [LoadAssets](#loadassets).

### <a name="update"></a>Aggiornamento

Aggiornare tutti gli elementi che devono essere modificati dall'ultimo frame.

-   Modificare la costante, il vertice, i buffer di indice e tutti gli altri elementi, se necessario.

Vedere [OnUpdate](#onupdate).

### <a name="render"></a>Rendering

Creare il nuovo mondo.

-   Popolare l'elenco di comandi.
    -   Reimpostare l'allocatore dell'elenco dei comandi.
        > [!Note]  
        > Riutilizzare la memoria associata all'allocatore di comandi.

         

    -   Reimpostare l'elenco dei comandi.
    -   Imposta la firma radice grafica.
        > [!Note]  
        > Imposta la firma radice grafica da usare per l'elenco di comandi corrente.

         

    -   Impostare il viewport e i rettangoli a forbice.
    -   Impostare una barriera delle risorse, che indica che il buffer nascosto deve essere usato come destinazione di rendering.
        > [!Note]  
        > Le barriere delle risorse vengono usate per gestire le transizioni delle risorse.

         

    -   Registrare i comandi nell'elenco dei comandi.
    -   Indica che il buffer nascosto verrà usato per presentare dopo l'esecuzione dell'elenco dei comandi.
        > [!Note]  
        > Un'altra chiamata per impostare una barriera delle risorse.

         

    -   Chiudere l'elenco dei comandi per eseguire ulteriori registrazioni.
-   Eseguire l'elenco dei comandi.
-   Presentare il frame.
-   Attendere il completamento della GPU.
    > [!Note]  
    > Continua ad aggiornare e controllare la recinzione.

Vedere [OnRender](#onrender).

### <a name="destroy"></a>Destroy

Chiudere l'app in modo semplice.

-   Attendere il completamento della GPU.
    > [!Note]  
    > Controllo finale sul perimetro.

-   Chiudere l'handle dell'evento.

Vedere [OnDestroy](#ondestroy).

## <a name="code-example-for-a-simple-app"></a>Esempio di codice per un'app semplice

Il codice seguente espande il flusso del codice sopra riportato per includere il codice richiesto per un esempio di base.

### <a name="class-d3d12hellotriangle"></a>Classe D3D12HelloTriangle

Definire prima di tutto la classe in un file di intestazione, inclusi un viewport, un rettangolo a forbice e un buffer vertex usando le strutture:

-   [**\_Viewport D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)
-   [**D3D12 \_ Rect**](d3d12-rect.md)
-   [**\_ \_ Visualizzazione buffer vertex \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)

```cpp
#include "DXSample.h"

using namespace DirectX;
using namespace Microsoft::WRL;

class D3D12HelloTriangle : public DXSample
{
public:
    D3D12HelloTriangle(UINT width, UINT height, std::wstring name);

    virtual void OnInit();
    virtual void OnUpdate();
    virtual void OnRender();
    virtual void OnDestroy();

private:
    static const UINT FrameCount = 2;

    struct Vertex
    {
        XMFLOAT3 position;
        XMFLOAT4 color;
    };

    // Pipeline objects.
    D3D12_VIEWPORT m_viewport;
    D3D12_RECT m_scissorRect;
    ComPtr<IDXGISwapChain3> m_swapChain;
    ComPtr<ID3D12Device> m_device;
    ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
    ComPtr<ID3D12CommandAllocator> m_commandAllocator;
    ComPtr<ID3D12CommandQueue> m_commandQueue;
    ComPtr<ID3D12RootSignature> m_rootSignature;
    ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
    ComPtr<ID3D12PipelineState> m_pipelineState;
    ComPtr<ID3D12GraphicsCommandList> m_commandList;
    UINT m_rtvDescriptorSize;

    // App resources.
    ComPtr<ID3D12Resource> m_vertexBuffer;
    D3D12_VERTEX_BUFFER_VIEW m_vertexBufferView;

    // Synchronization objects.
    UINT m_frameIndex;
    HANDLE m_fenceEvent;
    ComPtr<ID3D12Fence> m_fence;
    UINT64 m_fenceValue;

    void LoadPipeline();
    void LoadAssets();
    void PopulateCommandList();
    void WaitForPreviousFrame();
};
```

### <a name="oninit"></a>OnInit ()

Nel file di origine principale dei progetti avviare l'inizializzazione degli oggetti:

```cpp
void D3D12HelloTriangle::OnInit()
{
    LoadPipeline();
    LoadAssets();
}
```

### <a name="loadpipeline"></a>LoadPipeline()

Il codice seguente crea le nozioni di base per una pipeline grafica. Il processo di creazione di dispositivi e catene di scambio è molto simile a Direct3D 11.

-   Abilitare il livello di debug, con le chiamate a:<dl>

[**D3D12GetDebugInterface**](/windows/win32/api/d3d12/nf-d3d12-d3d12getdebuginterface)  
    [**ID3D12Debug::EnableDebugLayer**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)  
    </dl>
-   Creare il dispositivo:<dl>

[**CreateDXGIFactory1**](/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1)  
    [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)  
    </dl>
-   Compilare una descrizione della coda di comandi, quindi creare la coda dei comandi:<dl>

[**\_ \_ Descrizione coda comandi \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)  
    [**ID3D12Device::CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)  
    </dl>
-   Compilare una descrizione presentazione catena, quindi creare la catena di scambio: <dl>

[**\_ \_ desc catena di scambio DXGI \_**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)  
    [**IDXGIFactory::CreateSwapChain**](/windows/win32/api/dxgi/nf-dxgi-idxgifactory-createswapchain)  
    [**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)  
    </dl>
-   Compilare una descrizione dell'heap. creare quindi un heap del descrittore: <dl>

[**D3D12 \_ \_ Descrizione heap descrittore \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)  
    [**ID3D12Device::CreateDescriptorHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)  
    [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)  
    </dl>
-   Creare la visualizzazione della destinazione di rendering: <dl>

[**\_ \_ Handle descrittore CPU CD3DX12 \_**](cd3dx12-cpu-descriptor-handle.md)  
    [**GetCPUDescriptorHandleForHeapStart**](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [**IDXGISwapChain:: GetBuffer**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)  
    [**ID3D12Device::CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)  
    </dl>
-   Creare il comando allocator: [**ID3D12Device:: CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).

Nei passaggi successivi gli elenchi di comandi vengono ottenuti dall'allocatore di comandi e inviati alla coda dei comandi.

Caricare le dipendenze della pipeline di rendering (si noti che la creazione di un dispositivo WARP software è interamente facoltativa).


```cpp
void D3D12HelloTriangle::LoadPipeline()
{
#if defined(_DEBUG)
    // Enable the D3D12 debug layer.
    {
        
        ComPtr<ID3D12Debug> debugController;
        if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&debugController))))
        {
            debugController->EnableDebugLayer();
        }
    }
#endif

    ComPtr<IDXGIFactory4> factory;
    ThrowIfFailed(CreateDXGIFactory1(IID_PPV_ARGS(&factory)));

    if (m_useWarpDevice)
    {
        ComPtr<IDXGIAdapter> warpAdapter;
        ThrowIfFailed(factory->EnumWarpAdapter(IID_PPV_ARGS(&warpAdapter)));

        ThrowIfFailed(D3D12CreateDevice(
            warpAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }
    else
    {
        ComPtr<IDXGIAdapter1> hardwareAdapter;
        GetHardwareAdapter(factory.Get(), &hardwareAdapter);

        ThrowIfFailed(D3D12CreateDevice(
            hardwareAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }

    // Describe and create the command queue.
    D3D12_COMMAND_QUEUE_DESC queueDesc = {};
    queueDesc.Flags = D3D12_COMMAND_QUEUE_FLAG_NONE;
    queueDesc.Type = D3D12_COMMAND_LIST_TYPE_DIRECT;

    ThrowIfFailed(m_device->CreateCommandQueue(&queueDesc, IID_PPV_ARGS(&m_commandQueue)));

    // Describe and create the swap chain.
    DXGI_SWAP_CHAIN_DESC swapChainDesc = {};
    swapChainDesc.BufferCount = FrameCount;
    swapChainDesc.BufferDesc.Width = m_width;
    swapChainDesc.BufferDesc.Height = m_height;
    swapChainDesc.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
    swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
    swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_DISCARD;
    swapChainDesc.OutputWindow = Win32Application::GetHwnd();
    swapChainDesc.SampleDesc.Count = 1;
    swapChainDesc.Windowed = TRUE;

    ComPtr<IDXGISwapChain> swapChain;
    ThrowIfFailed(factory->CreateSwapChain(
        m_commandQueue.Get(),        // Swap chain needs the queue so that it can force a flush on it.
        &swapChainDesc,
        &swapChain
        ));

    ThrowIfFailed(swapChain.As(&m_swapChain));

    // This sample does not support fullscreen transitions.
    ThrowIfFailed(factory->MakeWindowAssociation(Win32Application::GetHwnd(), DXGI_MWA_NO_ALT_ENTER));

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();

    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
            rtvHandle.Offset(1, m_rtvDescriptorSize);
        }
    }

    ThrowIfFailed(m_device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocator)));
}
```



### <a name="loadassets"></a>LoadAssets()

Il caricamento e la preparazione degli asset è un processo lungo. Molte di queste fasi sono simili a D3D 11, anche se alcune sono nuove per D3D 12.

In Direct3D 12 lo stato della pipeline richiesto è associato a un elenco di comandi tramite un [oggetto di stato della pipeline](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO). Questo esempio illustra come creare un oggetto PSO. È possibile archiviare l'oggetto PSO come variabile membro e riutilizzarlo il numero di volte necessario.

Un heap descrittore definisce le visualizzazioni e come accedere alle risorse, ad esempio una visualizzazione della destinazione di rendering.

Con l'elenco dei comandi allocator e PSO, è possibile creare l'elenco di comandi effettivo, che verrà eseguito in un secondo momento.

Le API e i processi seguenti vengono chiamati in successione.

-   Creare una firma radice vuota, usando la struttura Helper disponibile: <dl>

[**\_Descrizione della \_ firma \_ radice CD3DX12**](cd3dx12-root-signature-desc.md)  
    [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)  
    [**ID3D12Device::CreateRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)  
    </dl>
-   Caricare e compilare gli shader: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).
-   Creare il layout di input del vertice: [**\_ elemento di input D3D12 \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).
-   Compilare una descrizione dello stato della pipeline, usando le strutture di supporto disponibili, quindi creare lo stato della pipeline grafica: <dl>

[**\_ \_ \_ Descrizione dello stato della pipeline grafica D3D12 \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)  
    [**CD3DX12 \_ rasterizzatore \_ DESC**](cd3dx12-rasterizer-desc.md)  
    [**CD3DX12 \_ Blend \_ DESC**](cd3dx12-blend-desc.md)  
    [**ID3D12Device::CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)  
    </dl>
-   Creare, quindi chiudere, un elenco di comandi: <dl>

[**ID3D12Device::CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)  
    [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)  
    </dl>
-   Creare il buffer vertex: [**ID3D12Device:: CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).
-   Copiare i dati dei vertici nel buffer dei vertici:<dl>

[**ID3D12Resource:: Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)  
    [**ID3D12Resource:: annullare**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-unmap)  
    </dl>
-   Inizializzare la visualizzazione del buffer dei vertici: [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).
-   Creare e inizializzare la recinzione: [**ID3D12Device:: CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).
-   Creare un handle di evento da usare con la sincronizzazione dei frame.
-   Attendere il completamento della GPU.


```cpp
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
        CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_UPLOAD);
        auto desc = CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize);
        ThrowIfFailed(m_device->CreateCommittedResource(
            &heapProps,
            D3D12_HEAP_FLAG_NONE,
            &desc,
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



### <a name="onupdate"></a>OnUpdate ()

Per un semplice esempio, non viene aggiornato alcun elemento.


```cpp
void D3D12HelloTriangle::OnUpdate()

{
}
```



### <a name="onrender"></a>OnRender ()

Durante la configurazione, la variabile membro **m \_ Commanding** è stata usata per registrare ed eseguire tutti i comandi di configurazione. È ora possibile riutilizzare il membro nel ciclo di rendering principale.

Il rendering prevede una chiamata per popolare l'elenco di comandi, quindi l'elenco dei comandi può essere eseguito e il buffer successivo nella catena di scambio presenta:

-   Popolare l'elenco di comandi.
-   Eseguire l'elenco di comandi: [**ID3D12CommandQueue:: oggetti executecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).
-   [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) il frame.
-   Attendere la fine della GPU.


```cpp
void D3D12HelloTriangle::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(1, 0));

    WaitForPreviousFrame();
}
```



### <a name="populatecommandlist"></a>PopulateCommandList()

È necessario reimpostare l'allocatore dell'elenco di comandi e l'elenco dei comandi prima di poterlo riutilizzare. Negli scenari più avanzati può essere utile reimpostare l'allocatore ogni più frame. La memoria è associata all'allocatore che non può essere rilasciata immediatamente dopo l'esecuzione di un elenco di comandi. Questo esempio illustra come reimpostare l'allocatore dopo ogni frame.

A questo punto, riutilizzare l'elenco dei comandi per il frame corrente. Riassegnare il viewport all'elenco dei comandi (che deve essere eseguito ogni volta che viene reimpostato un elenco di comandi e prima che venga eseguito l'elenco dei comandi), indicare che la risorsa verrà utilizzata come destinazione di rendering, registrare i comandi e indicare che la destinazione di rendering verrà utilizzata per presentare al termine dell'esecuzione dell'elenco dei comandi.

Il popolamento degli elenchi di comandi chiama a sua volta i metodi e i processi seguenti:

-   Reimpostare l'allocatore di comandi e l'elenco dei comandi: <dl>

[**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)  
    [**ID3D12GraphicsCommandList:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)  
    </dl>
-   Impostare i rettangoli di firma radice, viewport e forbici: <dl>

[**ID3D12GraphicsCommandList::SetGraphicsRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature)  
    [**ID3D12GraphicsCommandList::RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)  
    [**ID3D12GraphicsCommandList::RSSetScissorRects**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)  
    </dl>
-   Indica che il buffer nascosto deve essere utilizzato come destinazione di rendering: <dl>

[**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)  
    [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)  
    </dl>
-   Registrare i comandi:<dl>

[**ID3D12GraphicsCommandList::ClearRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)  
    [**ID3D12GraphicsCommandList::IASetPrimitiveTopology**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)  
    [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)  
    [**ID3D12GraphicsCommandList::D rawInstanced**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)  
    </dl>
-   Indica che il buffer nascosto verrà ora usato per presentare: [**ID3D12GraphicsCommandList:: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).
-   Chiudere l'elenco dei comandi: [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).


```cpp
void D3D12HelloTriangle::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated 
    // command lists have finished execution on the GPU; apps should use 
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocator->Reset());

    // However, when ExecuteCommandList() is called on a particular command 
    // list, that command list can then be reset at any time and must be before 
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());
    m_commandList->RSSetViewports(1, &m_viewport);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET);
    m_commandList->ResourceBarrier(1, &barrier);

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->DrawInstanced(3, 1, 0, 0);

    // Indicate that the back buffer will now be used to present.
    barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT);
    m_commandList->ResourceBarrier(1, &barrier);

    ThrowIfFailed(m_commandList->Close());
}
```



### <a name="waitforpreviousframe"></a>WaitForPreviousFrame()

Il codice seguente illustra un uso più semplificato delle recinzioni.

> [!Note]  
> In attesa del completamento di un frame è troppo inefficiente per la maggior parte delle app.

 

Le API e i processi seguenti vengono chiamati nell'ordine seguente:

-   [**ID3D12CommandQueue:: Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
-   [**ID3D12Fence::GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)
-   [**ID3D12Fence::SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)
-   Attendere l'evento.
-   Aggiornare l'indice del frame: [**IDXGISwapChain3:: GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).


```cpp
void D3D12HelloTriangle::WaitForPreviousFrame()
{
    // WAITING FOR THE FRAME TO COMPLETE BEFORE CONTINUING IS NOT BEST PRACTICE.
    // This is code implemented as such for simplicity. More advanced samples 
    // illustrate how to use fences for efficient resource usage.

    // Signal and increment the fence value.
    const UINT64 fence = m_fenceValue;
    ThrowIfFailed(m_commandQueue->Signal(m_fence.Get(), fence));
    m_fenceValue++;

    // Wait until the previous frame is finished.
    if (m_fence->GetCompletedValue() < fence)
    {
        ThrowIfFailed(m_fence->SetEventOnCompletion(fence, m_fenceEvent));
        WaitForSingleObject(m_fenceEvent, INFINITE);
    }

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();
}
```



### <a name="ondestroy"></a>OnDestroy ()

Chiudere l'app in modo semplice.

-   Attendere il completamento della GPU.
-   Chiudere l'evento.


```cpp
void D3D12HelloTriangle::OnDestroy()
{

    // Wait for the GPU to be done with all resources.
    WaitForPreviousFrame();

    CloseHandle(m_fenceEvent);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Esempi di lavoro](working-samples.md)
</dt> </dl>

 

 
