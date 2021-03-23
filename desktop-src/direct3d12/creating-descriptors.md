---
title: Creazione di descrittori
description: Vengono descritti e illustrati esempi per la creazione di viste di buffer di indice, vertex e costanti; risorsa shader, destinazione di rendering, accesso non ordinato, output del flusso e visualizzazioni di stencil Depth; e Samplers. Tutti i metodi per la creazione di descrittori sono a thread libero.
ms.assetid: 0D360A7C-8A2F-49E1-A5CC-98C958B59D1C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aac9aab5dde0f5ca0864fcc1627ade984c6b6ccf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548821"
---
# <a name="creating-descriptors"></a>Creazione di descrittori

Vengono descritti e illustrati esempi per la creazione di viste di buffer di indice, vertex e costanti; risorsa shader, destinazione di rendering, accesso non ordinato, output del flusso e visualizzazioni di stencil Depth; e Samplers. Tutti i metodi per la creazione di descrittori sono a thread libero.

-   [Visualizzazione buffer indice](#index-buffer-view)
-   [Visualizzazione buffer vertici](#vertex-buffer-view)
-   [Shader Resource View](#shader-resource-view)
-   [Constant Buffer View](#constant-buffer-view)
-   [Campionatore](#sampler)
-   [Unordered Access View](#unordered-access-view)
-   [Visualizzazione output flusso](#stream-output-view)
-   [Visualizzazione destinazione rendering](#render-target-view)
-   [Visualizzazione stencil profondità](#depth-stencil-view)
-   [Argomenti correlati](#related-topics)

## <a name="index-buffer-view"></a>Visualizzazione buffer indice

Per creare una visualizzazione buffer dell'indice, compilare una struttura di [**\_ \_ \_ visualizzazione buffer dell'indice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view) :

``` syntax
typedef struct D3D12_INDEX_BUFFER_VIEW
{
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
    UINT SizeInBytes;
    DXGI_FORMAT Format;
}   D3D12_INDEX_BUFFER_VIEW;
```

Impostare il percorso (Call [**GetGPUVirtualAddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) e la dimensione del buffer, notando che l' \_ indirizzo virtuale della GPU D3D12 \_ \_ è definito come:

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

Vedere l'enumerazione [**del \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) . In genere, per un buffer di indice è possibile usare la definizione seguente:

`const DXGI_FORMAT StandardIndexFormat = DXGI_FORMAT_R32_UINT;`

Infine, chiamare [**ID3D12GraphicsCommandList:: IASetIndexBuffer**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer).

Ad esempio,


```C++
// Initialize the index buffer view.
m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
```



## <a name="vertex-buffer-view"></a>Visualizzazione buffer vertici

Per creare una visualizzazione del buffer dei vertici, compilare una struttura di [**\_ visualizzazione del \_ buffer \_ dei vertici di D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view) :

``` syntax
typedef struct D3D12_VERTEX_BUFFER_VIEW {
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;  
    UINT SizeInBytes;  
    UINT StrideInBytes;  
} D3D12_VERTEX_BUFFER_VIEW;
```

Impostare il percorso (Call [**GetGPUVirtualAddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) e la dimensione del buffer, notando che l' \_ indirizzo virtuale della GPU D3D12 \_ \_ è definito come:

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

Lo stride corrisponde in genere alla dimensione di una struttura di dati di un singolo vertice, ad esempio `sizeof(Vertex);` , quindi chiama [**ID3D12GraphicsCommandList:: IASetVertexBuffers**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers).

Ad esempio,


```C++
// Initialize the vertex buffer view.
m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
m_vertexBufferView.SizeInBytes = SampleAssets::VertexDataSize;
m_vertexBufferView.StrideInBytes = SampleAssets::StandardVertexStride;
```



## <a name="shader-resource-view"></a>Shader Resource View

Per creare una visualizzazione risorse dello shader, compilare una struttura [**di \_ \_ \_ visualizzazione \_ delle risorse shader D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) :

``` syntax
typedef struct D3D12_SHADER_RESOURCE_VIEW_DESC  
    {  
    DXGI_FORMAT Format;  
    D3D12_SRV_DIMENSION ViewDimension;  
    UINT Shader4ComponentMapping;  
    union   
        {  
        D3D12_BUFFER_SRV Buffer;  
        D3D12_TEX1D_SRV Texture1D;  
        D3D12_TEX1D_ARRAY_SRV Texture1DArray;  
        D3D12_TEX2D_SRV Texture2D;  
        D3D12_TEX2D_ARRAY_SRV Texture2DArray;  
        D3D12_TEX2DMS_SRV Texture2DMS;  
        D3D12_TEX2DMS_ARRAY_SRV Texture2DMSArray;  
        D3D12_TEX3D_SRV Texture3D;  
        D3D12_TEXCUBE_SRV TextureCube;  
        D3D12_TEXCUBE_ARRAY_SRV TextureCubeArray;  
        }   ;  
    }   D3D12_SHADER_RESOURCE_VIEW_DESC; 
```

Il `ViewDimension` campo è impostato su zero o un valore dell'enumerazione dei [**\_ \_ \_ flag SRV del buffer D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags) .

Le enumerazioni e le strutture a cui fa riferimento la [**\_ \_ \_ vista risorse \_ shader D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) sono:

-   [**\_formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**\_SRV buffer \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv)
-   [**D3D12 \_ TEX1D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv)
-   [**D3D12 \_ TEX1D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_srv)
-   [**D3D12 \_ TEX2DMS \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX3D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_srv)
-   [**D3D12 \_ TEXCUBE \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_srv)
-   [**D3D12 \_ TEXCUBE \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_array_srv)

Si noti che il float `ResourceMinLODClamp` è stato aggiunto a SRVs per Tex1D/2D/3D/Cube. In D3D11, si trattava di una proprietà di una risorsa, ma non corrispondeva al modo in cui è stata implementata nell'hardware. `StructureByteStride` è stato aggiunto a buffer SRVs, dove in D3D11 era una proprietà della risorsa. Se stride è diverso da zero, che indica una visualizzazione strutturata del buffer e il formato deve essere impostato su DXGI \_ Format \_ Unknown.

Infine, per creare la visualizzazione risorse dello shader, chiamare [**ID3D12Device:: CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview).

Ad esempio,


```C++
// Describe and create an SRV.
D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
srvDesc.Format = tex.Format;
srvDesc.Texture2D.MipLevels = tex.MipLevels;
srvDesc.Texture2D.MostDetailedMip = 0;
srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);
```



## <a name="constant-buffer-view"></a>Constant Buffer View

Per creare una visualizzazione del buffer costante, compilare una struttura di [**\_ \_ \_ visualizzazione \_ del buffer costante D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc) :

``` syntax
typedef struct D3D12_CONSTANT_BUFFER_VIEW_DESC {
  D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
  UINT   SizeInBytes;
} D3D12_CONSTANT_BUFFER_VIEW_DESC;
```

Quindi, chiamare [**ID3D12Device:: CreateConstantBufferView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview).

Ad esempio,


```C++
// Describe and create a constant buffer view.
D3D12_CONSTANT_BUFFER_VIEW_DESC cbvDesc = {};
cbvDesc.BufferLocation = m_constantBuffer->GetGPUVirtualAddress();
cbvDesc.SizeInBytes = (sizeof(ConstantBuffer) + 255) & ~255;    // CB size is required to be 256-byte aligned.
m_device->CreateConstantBufferView(&cbvDesc, m_cbvHeap->GetCPUDescriptorHandleForHeapStart());
```



## <a name="sampler"></a>Campionatore

Per creare un esempio, compilare una struttura [**D3D12 \_ Sampler \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc) :

``` syntax
typedef struct D3D12_SAMPLER_DESC
{
    D3D12_FILTER Filter;
    D3D12_TEXTURE_ADDRESS_MODE AddressU;
    D3D12_TEXTURE_ADDRESS_MODE AddressV;
    D3D12_TEXTURE_ADDRESS_MODE AddressW;
    FLOAT MipLODBias;
    UINT MaxAnisotropy;
    D3D12_COMPARISON_FUNC ComparisonFunc;
    FLOAT BorderColor[4]; // RGBA
    FLOAT MinLOD;
    FLOAT MaxLOD;
} D3D12_SAMPLER_DESC;
```

Per compilare questa struttura, fare riferimento alle enumerazioni seguenti:

-   [**\_Filtro D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)
-   [**\_Tipo di filtro D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_type)
-   [**\_Tipo di \_ riduzione del filtro D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_reduction_type)
-   [**\_Modalità di \_ indirizzamento della trama D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode)
-   [**Funzione di \_ confronto D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)

Infine, chiamare [**ID3D12Device:: CreateSampler**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler).

Ad esempio,


```C++
// Describe and create a sampler.
D3D12_SAMPLER_DESC samplerDesc = {};
samplerDesc.Filter = D3D12_FILTER_MIN_MAG_MIP_LINEAR;
samplerDesc.AddressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.AddressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.AddressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.MinLOD = 0;
samplerDesc.MaxLOD = D3D12_FLOAT32_MAX;
samplerDesc.MipLODBias = 0.0f;
samplerDesc.MaxAnisotropy = 1;
samplerDesc.ComparisonFunc = D3D12_COMPARISON_FUNC_ALWAYS;
m_device->CreateSampler(&samplerDesc, m_samplerHeap->GetCPUDescriptorHandleForHeapStart());
```



## <a name="unordered-access-view"></a>Unordered Access View

Per creare una visualizzazione di accesso non ordinata, compilare una struttura [**D3D12 non \_ ordinata della vista di \_ accesso \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc) :

``` syntax
typedef struct D3D12_UNORDERED_ACCESS_VIEW_DESC
{
    DXGI_FORMAT Format;
    D3D12_UAV_DIMENSION ViewDimension;

    union
    {
        D3D12_BUFFER_UAV Buffer;
        D3D12_TEX1D_UAV Texture1D;
        D3D12_TEX1D_ARRAY_UAV Texture1DArray;
        D3D12_TEX2D_UAV Texture2D;
        D3D12_TEX2D_ARRAY_UAV Texture2DArray;
        D3D12_TEX3D_UAV Texture3D;
    };
} D3D12_UNORDERED_ACCESS_VIEW_DESC;
```

Il `ViewDimension` campo è impostato su zero o un valore dell'enumerazione dei [**\_ \_ \_ flag UAV del buffer D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) .

Vedere le enumerazioni e le strutture seguenti:

-   [**\_formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**\_UAV buffer \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX1D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEX2D \_ array \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

`StructureByteStride` è stato aggiunto a buffer UAV, dove in D3D11 era una proprietà della risorsa. Se stride è diverso da zero, che indica una visualizzazione strutturata del buffer e il formato deve essere impostato su DXGI \_ Format \_ Unknown.

Infine, chiamare [**ID3D12Device:: CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).

Ad esempio,


```C++
// Create the unordered access views (UAVs) that store the results of the compute work.
CD3DX12_CPU_DESCRIPTOR_HANDLE processedCommandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), ProcessedCommandsOffset, m_cbvSrvUavDescriptorSize);
for (UINT frame = 0; frame < FrameCount; frame++)
{
    // Allocate a buffer large enough to hold all of the indirect commands
    // for a single frame as well as a UAV counter.
    commandBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(CommandBufferSizePerFrame + sizeof(UINT), D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS);
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &commandBufferDesc,
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_processedCommandBuffers[frame])));

    D3D12_UNORDERED_ACCESS_VIEW_DESC uavDesc = {};
    uavDesc.Format = DXGI_FORMAT_UNKNOWN;
    uavDesc.ViewDimension = D3D12_UAV_DIMENSION_BUFFER;
    uavDesc.Buffer.FirstElement = 0;
    uavDesc.Buffer.NumElements = TriangleCount;
    uavDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
    uavDesc.Buffer.CounterOffsetInBytes = CommandBufferSizePerFrame;
    uavDesc.Buffer.Flags = D3D12_BUFFER_UAV_FLAG_NONE;

    m_device->CreateUnorderedAccessView(            
        m_processedCommandBuffers[frame].Get(),
        m_processedCommandBuffers[frame].Get(),
        &uavDesc,
        processedCommandsHandle);

    processedCommandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
}

// Allocate a buffer that can be used to reset the UAV counters and initialize it to 0.
ThrowIfFailed(m_device->CreateCommittedResource(
    &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
    D3D12_HEAP_FLAG_NONE,
    &CD3DX12_RESOURCE_DESC::Buffer(sizeof(UINT)),
    D3D12_RESOURCE_STATE_GENERIC_READ,
    
    nullptr,
    IID_PPV_ARGS(&m_processedCommandBufferCounterReset)));

UINT8* pMappedCounterReset = nullptr;
CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
ThrowIfFailed(m_processedCommandBufferCounterReset->Map(0, &readRange, reinterpret_cast<void**>(&pMappedCounterReset)));
ZeroMemory(pMappedCounterReset, sizeof(UINT));
m_processedCommandBufferCounterReset->Unmap(0, nullptr);
```



## <a name="stream-output-view"></a>Visualizzazione output flusso

Per creare una visualizzazione di output del flusso, compilare una struttura [**\_ \_ \_ desc di output**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) del flusso D3D12.

``` syntax
typedef struct D3D12_STREAM_OUTPUT_DESC  
    {  
    _Field_size_full_(NumEntries)  const D3D12_SO_DECLARATION_ENTRY *pSODeclaration;  
    UINT NumEntries;  
    _Field_size_full_(NumStrides)  const UINT *pBufferStrides;  
    UINT NumStrides;  
    UINT RasterizedStream;  
    }   D3D12_STREAM_OUTPUT_DESC;  
```

Quindi, chiamare [**ID3D12GraphicsCommandList:: SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets).

## <a name="render-target-view"></a>Visualizzazione destinazione rendering

Per creare una visualizzazione della destinazione di rendering, compilare una struttura di [**\_ visualizzazione della destinazione di rendering \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc) .

``` syntax
typedef struct D3D12_RENDER_TARGET_VIEW_DESC
{
    DXGI_FORMAT Format;
    D3D12_RTV_DIMENSION ViewDimension;

    union
    {
        D3D12_BUFFER_RTV Buffer;
        D3D12_TEX1D_RTV Texture1D;
        D3D12_TEX1D_ARRAY_RTV Texture1DArray;
        D3D12_TEX2D_RTV Texture2D;
        D3D12_TEX2D_ARRAY_RTV Texture2DArray;
        D3D12_TEX2DMS_RTV Texture2DMS;
        D3D12_TEX2DMS_ARRAY_RTV Texture2DMSArray;
        D3D12_TEX3D_RTV Texture3D;
    };
} D3D12_RENDER_TARGET_VIEW_DESC;
```

Il `ViewDimension` campo è impostato su zero o su un valore dell'enumerazione [**D3D12 \_ RTV \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_rtv_dimension) .

Vedere le enumerazioni e le strutture seguenti:

-   [**\_formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 \_ buffer \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_rtv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX1D \_ array \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2DMS \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv)
-   [**D3D12 \_ TEX2D \_ array \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2DMS \_ array \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)

Infine, chiamare [**ID3D12Device:: CreateRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview).

Ad esempio,

```C++
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
```



## <a name="depth-stencil-view"></a>Visualizzazione stencil profondità

Per creare una visualizzazione depth stencil, compilare una struttura [**D3D12 \_ Depth \_ stencil \_ View \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc) :

``` syntax
typedef struct D3D12_DEPTH_STENCIL_VIEW_DESC  
    {  
    DXGI_FORMAT Format;  
    D3D12_DSV_DIMENSION ViewDimension;  
    D3D12_DSV_FLAGS Flags;  
    union   
        {  
        D3D12_TEX1D_DSV Texture1D;  
        D3D12_TEX1D_ARRAY_DSV Texture1DArray;  
        D3D12_TEX2D_DSV Texture2D;  
        D3D12_TEX2D_ARRAY_DSV Texture2DArray;  
        D3D12_TEX2DMS_DSV Texture2DMS;  
        D3D12_TEX2DMS_ARRAY_DSV Texture2DMSArray;  
        }   ;  
    }   D3D12_DEPTH_STENCIL_VIEW_DESC;  
```

Il `ViewDimension` campo è impostato su zero o su un valore dell'enumerazione [**D3D12 \_ della \_ dimensione DSV**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_dimension) . Per le impostazioni dei flag, vedere l'enumerazione dei [**\_ \_ flag DSV D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_flags) .

Vedere le enumerazioni e le strutture seguenti:

-   [**\_formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**Vista \_ origine dati TEX1D D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**Vista \_ \_ origine dati matrice TEX1D D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**Vista \_ origine dati TEX2D D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**Vista \_ \_ origine dati matrice TEX2D D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**Vista \_ origine dati TEX2DMS D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv)
-   [**Vista \_ \_ origine dati matrice TEX2DMS D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)

Infine, chiamare [**ID3D12Device:: CreateDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview).

Ad esempio,


```C++
// Create the depth stencil view.
{
    D3D12_DEPTH_STENCIL_VIEW_DESC depthStencilDesc = {};
    depthStencilDesc.Format = DXGI_FORMAT_D32_FLOAT;
    depthStencilDesc.ViewDimension = D3D12_DSV_DIMENSION_TEXTURE2D;
    depthStencilDesc.Flags = D3D12_DSV_FLAG_NONE;

    D3D12_CLEAR_VALUE depthOptimizedClearValue = {};
    depthOptimizedClearValue.Format = DXGI_FORMAT_D32_FLOAT;
    depthOptimizedClearValue.DepthStencil.Depth = 1.0f;
    depthOptimizedClearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Tex2D(DXGI_FORMAT_D32_FLOAT, m_width, m_height, 1, 0, 1, 0, D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL),
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &depthOptimizedClearValue,
        IID_PPV_ARGS(&m_depthStencil)
        ));

    m_device->CreateDepthStencilView(m_depthStencil.Get(), &depthStencilDesc, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Descrittori](descriptors.md)
</dt> <dt>

[Heap descrittore](descriptor-heaps.md)
</dt> </dl>

 

 