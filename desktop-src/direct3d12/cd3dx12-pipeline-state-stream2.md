---
title: CD3DX12_PIPELINE_STATE_STREAM2 struttura (D3dx12.h)
description: Struttura helper per la creazione e l'uso degli stati della pipeline grafica e di calcolo tramite un'interfaccia combinata.
keywords:
- CD3DX12_PIPELINE_STATE_STREAM2 struttura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM2
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: 18b662217f5e2a59c7925e0f401a9288ea710e8a
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812337"
---
# <a name="cd3dx12_pipeline_state_stream2-structure"></a>CD3DX12_PIPELINE_STATE_STREAM2 struttura

Struttura helper per la creazione e l'uso degli stati della pipeline grafica e di calcolo tramite un'interfaccia combinata. Vedere [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

**CD3DX12_PIPELINE_STATE_STREAM2** supporta la build del sistema operativo 19041+ (in cui è presente una pipeline mesh shader).

## <a name="syntax"></a>Sintassi

```cpp
struct CD3DX12_PIPELINE_STATE_STREAM2
{
    CD3DX12_PIPELINE_STATE_STREAM2();
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS Flags;
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK NodeMask;
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE pRootSignature;
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT InputLayout;
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE IBStripCutValue;
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY PrimitiveTopologyType;
    CD3DX12_PIPELINE_STATE_STREAM_VS VS;
    CD3DX12_PIPELINE_STATE_STREAM_GS GS;
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT StreamOutput;
    CD3DX12_PIPELINE_STATE_STREAM_HS HS;
    CD3DX12_PIPELINE_STATE_STREAM_DS DS;
    CD3DX12_PIPELINE_STATE_STREAM_PS PS;
    CD3DX12_PIPELINE_STATE_STREAM_AS AS;
    CD3DX12_PIPELINE_STATE_STREAM_MS MS;
    CD3DX12_PIPELINE_STATE_STREAM_CS CS;
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC BlendState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 DepthStencilState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT DSVFormat;
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER RasterizerState;
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC SampleDesc;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK SampleMask;
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO CachedPSO;
    CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING ViewInstancingDesc;
    D3D12_GRAPHICS_PIPELINE_STATE_DESC GraphicsDescV0() const noexcept;
    D3D12_COMPUTE_PIPELINE_STATE_DESC ComputeDescV0() const noexcept;
};
```

## <a name="members"></a>Members

`CD3DX12_PIPELINE_STATE_STREAM2`

Costruttore predefinito. Crea una nuova istanza non inizializzata di un **CD3DX12_PIPELINE_STATE_STREAM2**.

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC&)`

Costruttore che crea una nuova istanza di un **CD3DX12_PIPELINE_STATE_STREAM2** inizializzato con il contenuto di una [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) struttura .

Sarà quindi necessario impostare manualmente gli shader mesh e di amplificazione, perché non hanno una **rappresentazione** in D3D12_GRAPHICS_PIPELINE_STATE_DESC .

`CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC&)`

Costruttore che crea una nuova istanza di un **CD3DX12_PIPELINE_STATE_STREAM2** inizializzato con il contenuto di una [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) struttura .

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC&)`

Costruttore che crea una nuova istanza di un **CD3DX12_PIPELINE_STATE_STREAM2** inizializzato con il contenuto di una [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) struttura .

`Flags`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_FLAGS](cd3dx12-pipeline-state-stream-flags.md)**

Flag (ad esempio, per indicare che lo stato della pipeline deve essere compilato con informazioni aggiuntive per facilitare il debug).

`NodeMask`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK](cd3dx12-pipeline-state-stream-node-mask.md)**

Descrive la maschera del nodo dello stato della pipeline, usata per identificare i nodi (schede fisiche del dispositivo) a cui si applica PSO in scenari con più schede. ogni bit nella maschera corrisponde a un singolo nodo. Per gli scenari a scheda singola, usare 0.

`pRootSignature`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE](cd3dx12-pipeline-state-stream-root-signature.md)**

Descrive la firma radice.

`InputLayout`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT](cd3dx12-pipeline-state-stream-input-layout.md)**

Descrive il formato del buffer di input per la fase input-assembler

`IBStripCutValue`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)**

Descrive il valore di indice speciale del buffer di input che indica un taglio (discontinuità) quando si usa la topologia a striscia triangolare.

`PrimitiveTopologyType`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY](cd3dx12-pipeline-state-stream-primitive-topology.md)**

Descrive la topologia primitiva e il relativo ordine.

`VS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_VS](cd3dx12-pipeline-state-stream-vs.md)**

Descrive il vertex shader.

`GS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_GS](cd3dx12-pipeline-state-stream-gs.md)**

Descrive lo shader geometry.

`StreamOutput`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT](cd3dx12-pipeline-state-stream-stream-output.md)**

Descrive il buffer di output di streaming.

`HS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_HS](cd3dx12-pipeline-state-stream-hs.md)**

Descrive lo shader di tipo hull.

`DS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_DS](cd3dx12-pipeline-state-stream-ds.md)**

Descrive lo shader del dominio.

`PS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_PS](cd3dx12-pipeline-state-stream-ps.md)**

Viene descritta la pixel shader.

`AS`

Tipo: **CD3DX12_PIPELINE_STATE_STREAM_AS**

Descrive lo shader di amplificazione.

`MS`

Tipo: **CD3DX12_PIPELINE_STATE_STREAM_MS**

Descrive lo shader mesh.

`CS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_CS](cd3dx12-pipeline-state-stream-cs.md)**

Descrive il compute shader.

`BlendState`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC](cd3dx12-pipeline-state-stream-blend-desc.md)**

Descrive lo stato di blend.

`DepthStencilState`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1](cd3dx12-pipeline-state-stream-depth-stencil1.md)**

Descrive lo stato dello stencil di profondità.

`DSVFormat`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT](cd3dx12-pipeline-state-stream-depth-stencil-format.md)**

Descrive il formato dello stencil di profondità.

`RasterizerState`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER](cd3dx12-pipeline-state-stream-rasterizer.md)**

Descrive lo stato di rasterizzazione.

`RTVFormats`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS](cd3dx12-pipeline-state-stream-render-target-formats.md)**

Descrive i formati di destinazione di rendering.

`SampleDesc`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC](cd3dx12-pipeline-state-stream-sample-desc.md)**

Descrive il numero e la qualità dei campioni.

`SampleMask`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK](cd3dx12-pipeline-state-stream-sample-mask.md)**

Descrive la maschera di esempio usata con lo stato di blend.

`CachedPSO`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO](cd3dx12-pipeline-state-stream-cached-pso.md)**

Descrive un oggetto PSO memorizzato nella cache.

`ViewInstancingDesc`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING](cd3dx12-pipeline-state-stream-view-instancing.md)**

Descrive una configurazione di istanze della vista.

`GraphicsDescV0`

Restituisce [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc).

restituisce il contenuto **dell'oggetto CD3DX12_PIPELINE_STATE_STREAM2** come D3D12_GRAPHICS_PIPELINE_STATE_DESC struttura in base al valore.  **D3D12_GRAPHICS_PIPELINE_STATE_DESC** non include il membro *CS,* quindi il valore viene perso nella conversione.

`ComputeDescV0`

Restituisce [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

restituisce il contenuto **dell'oggetto CD3DX12_PIPELINE_STATE_STREAM2** come struttura **D3D12_COMPUTE_PIPELINE_STATE_DESC** per valore. **D3D12_COMPUTE_PIPELINE_STATE_DESC** non include i membri *InputLayout*, *IBStripCutValue*, *PrimitiveTopologyType*, *VS*, *GS*, *StreamOutput*, *HS*, *DS*, *PS*, *BlendState*, *DepthStencilState*, *DSVFormat*, *RasterizerState*, *NumRootSignature*, *RTVFormats*, *SampleDesc* e *SampleMask*, in modo che tali valori andranno persi nella conversione.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vedi anche

* [Strutture helper per Direct3D 12](helper-structures-for-d3d12.md)
