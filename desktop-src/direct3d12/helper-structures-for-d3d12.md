---
title: Strutture helper per Direct3D 12
description: Queste strutture helper consentono di inizializzare molte delle strutture Direct3D 12. Vengono dichiarati in `d3dx12.h` .
ms.assetid: 822CACCE-4A45-4104-91BD-4968A657662E
keywords:
- Strutture helper
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 07/28/2021
ms.openlocfilehash: 16dfa0349a815a07db810d67c21747cb767f7c39
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812371"
---
# <a name="helper-structures-for-direct3d-12"></a>Strutture helper per Direct3D 12

Queste strutture helper consentono di inizializzare molte delle strutture Direct3D 12. Vengono dichiarati in `d3dx12.h` .

`d3dx12.h` è disponibile separatamente dalle intestazioni Direct3D 12. È possibile scaricare `d3dx12.h` dalla [libreria helper D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**CD3DX12_BLEND_DESC**](cd3dx12-blend-desc.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc) struttura . |
| [**CD3DX12_BOX**](cd3dx12-box.md) | Struttura helper per consentire una facile inizializzazione di una [**D3D12_BOX**](/windows/win32/api/d3d12/ns-d3d12-d3d12_box) struttura . |
| [**CD3DX12_CLEAR_VALUE**](cd3dx12-clear-value.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_CLEAR_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value) struttura . |
| [**CD3DX12_CPU_DESCRIPTOR_HANDLE**](cd3dx12-cpu-descriptor-handle.md) | Struttura helper per consentire una facile inizializzazione di una [**struttura D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) di supporto. |
| [**CD3DX12_DEFAULT**](cd3dx12-default.md) | Passa **D3D12_DEFAULT** in un costruttore per ogni struttura helper. Questa struttura viene semplicemente usata come meccanismo per impostare i parametri predefiniti nelle altre strutture helper. |
| [**CD3DX12_DEPTH_STENCIL_DESC**](cd3dx12-depth-stencil-desc.md) | Struttura helper per consentire una facile inizializzazione di una [**D3D12_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) struttura . |
| [**CD3DX12_DEPTH_STENCIL_DESC1**](cd3dx12-depth-stencil-desc1.md) | Struttura helper per consentire una facile inizializzazione di una [**D3D12_DEPTH_STENCIL_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) struttura . |
| [**CD3DX12_DESCRIPTOR_RANGE**](cd3dx12-descriptor-range.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_DESCRIPTOR_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range) struttura . |
| [**CD3DX12_DESCRIPTOR_RANGE1**](cd3dx12-descriptor-range1.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_DESCRIPTOR_RANGE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range1) struttura . |
| [**CD3DX12_DXIL_LIBRARY_SUBOBJECT**](cd3dx12-dxil-library-subobject.md) | Classe helper per la creazione di un sottooggetto di stato della libreria DXIL. |
| [**CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION**](cd3dx12-dxil-subobject-to-exports-association.md) | Classe helper per la creazione di un sottooggetto DXIL-subobject-to-exports association state. |
| [**CD3DX12_EXISTING_COLLECTION_SUBOBJECT**](cd3dx12-existing-collection-subobject.md) | Classe helper per la creazione di un sottooggetto dello stato della raccolta esistente. |
| [**CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-global-root-signature-subobject.md) | Classe helper per la creazione di un suboject dello stato della firma radice globale. |
| [**CD3DX12_GPU_DESCRIPTOR_HANDLE**](cd3dx12-gpu-descriptor-handle.md) | Struttura helper per consentire una facile inizializzazione di una [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) struttura . |
| [**CD3DX12_HEAP_DESC**](cd3dx12-heap-desc.md) | Struttura helper per consentire una facile inizializzazione di una [**D3D12_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_desc) struttura . |
| [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_HEAP_PROPERTIES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) struttura . |
| [**CD3DX12_HIT_GROUP_SUBOBJECT**](cd3dx12-hit-group-subobject.md) | Classe helper per la creazione di un sottooggetto di stato del gruppo di hit. |
| [**CD3DX12_NODE_MASK_SUBOBJECT**](cd3dx12-node-mask-subobject.md) | Classe helper per la creazione di un sottooggetto di stato che identifica i nodi GPU a cui si applica l'oggetto stato. |
| [**CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-local-root-signature-subobject.md) | Classe helper per la creazione di un suboject dello stato della firma radice locale. |
| [**CD3DX12_PACKED_MIP_INFO**](cd3dx12-packed-mip-info.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_PACKED_MIP_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_packed_mip_info) struttura . |
| [**CD3DX12_PIPELINE_STATE_STREAM**](cd3dx12-pipeline-state-stream.md) | Struttura helper per la creazione e l'uso degli stati della pipeline grafica e di calcolo tramite un'interfaccia combinata. Vedere [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). |
| [**CD3DX12_PIPELINE_STATE_STREAM1**](cd3dx12-pipeline-state-stream1.md) | Struttura helper per la creazione e l'uso degli stati della pipeline grafica e di calcolo tramite un'interfaccia combinata. Vedere [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). |
| [**CD3DX12_PIPELINE_STATE_STREAM2**](cd3dx12-pipeline-state-stream2.md) | Struttura helper per la creazione e l'uso degli stati della pipeline grafica e di calcolo tramite un'interfaccia combinata. |
| [**CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) | Struttura helper usata per descrivere una descrizione di blend come un singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO**](cd3dx12-pipeline-state-stream-cached-pso.md) | Struttura helper usata per descrivere un oggetto PSO memorizzato nella cache come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_CS**](cd3dx12-pipeline-state-stream-cs.md) | Struttura helper usata per descrivere uno shader di calcolo come un singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md) | Struttura helper usata per descrivere una descrizione depth stencil come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md) | Struttura helper usata per descrivere una descrizione depth stencil come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT**](cd3dx12-pipeline-state-stream-depth-stencil-format.md) | Struttura helper usata per descrivere il formato depth stencil come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DS**](cd3dx12-pipeline-state-stream-ds.md) | Struttura helper usata per descrivere uno shader di dominio come un singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_FLAGS**](cd3dx12-pipeline-state-stream-flags.md) | Struttura helper usata per descrivere i flag di stato della pipeline come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_GS**](cd3dx12-pipeline-state-stream-gs.md) | Struttura helper usata per descrivere un geometry shader come un singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_HS**](cd3dx12-pipeline-state-stream-hs.md) | Struttura helper usata per descrivere uno hull shader come un singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md) | Struttura helper usata per descrivere il valore index buffer strip cut come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT**](cd3dx12-pipeline-state-stream-input-layout.md) | Struttura helper usata per descrivere un layout di input come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK**](cd3dx12-pipeline-state-stream-node-mask.md) | Struttura helper usata per descrivere una maschera di nodo come un singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER**](cd3dx12-pipeline-state-stream-parse-helper.md) | Compila un oggetto CD3DX12_PIPELINE_STATE_STREAM interno dai dettagli del sottooggetto passati alle funzioni membro corrispondenti. Questo struct implementa [**l'interfaccia ID3DX12PipelineParserCallbacks.**](id3dx12pipelineparsercallbacks.md) |
| [**CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY**](cd3dx12-pipeline-state-stream-primitive-topology.md) | Struttura helper usata per descrivere la topologia primitiva come un singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_PS**](cd3dx12-pipeline-state-stream-ps.md) | Struttura helper usata per descrivere un pixel shader come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) | Struttura helper usata per descrivere una descrizione del rasterizzatore come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS**](cd3dx12-pipeline-state-stream-render-target-formats.md) | Struttura helper usata per descrivere i formati di destinazione di rendering come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE**](cd3dx12-pipeline-state-stream-root-signature.md) | Struttura helper utilizzata per descrivere la firma radice come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC**](cd3dx12-pipeline-state-stream-sample-desc.md) | Struttura helper utilizzata per descrivere una descrizione di esempio come singolo oggetto adatto a una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK**](cd3dx12-pipeline-state-stream-sample-mask.md) | Struttura helper utilizzata per descrivere una maschera di esempio come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT**](cd3dx12-pipeline-state-stream-stream-output.md) | Struttura helper utilizzata per descrivere la descrizione dell'output del flusso come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) | Struttura helper modello utilizzata per incapsulare coppie di dati di tipo oggetto secondario e oggetto secondario come singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING**](cd3dx12-pipeline-state-stream-view-instancing.md) | Struttura helper utilizzata per eseguire il wrapping di [una CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) struttura . Consente agli shader di eseguire il rendering in più visualizzazioni con una singola chiamata di disegno. è utile per la visione stereo o la generazione di mappe cubi. |
| [**CD3DX12_PIPELINE_STATE_STREAM_VS**](cd3dx12-pipeline-state-stream-vs.md) | Struttura helper usata per descrivere un vertex shader come un singolo oggetto adatto per una descrizione del flusso. |
| [**CD3DX12_RANGE**](cd3dx12-range.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range) struttura . |
| [**CD3DX12_RANGE_UINT64**](cd3dx12-range-uint64.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range_uint64) struttura . |
| [**CD3DX12_RASTERIZER_DESC**](cd3dx12-rasterizer-desc.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_RASTERIZER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) struttura . |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT**](cd3dx12-raytracing-pipeline-config-subobject.md) | Classe helper per la creazione di un oggetto secondario dello stato di configurazione della pipeline di raytracing. |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT**](cd3dx12-raytracing-pipeline-config1-subobject.md) | Classe helper per la creazione di un oggetto secondario dello stato di configurazione della pipeline di raytracing, con flag. |
| [**CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT**](cd3dx12-raytracing-shader-config-subobject.md) | Classe helper per la creazione di un oggetto secondario dello stato di configurazione dello shader raytracing. |
| [**CD3DX12_RECT**](cd3dx12-rect.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_RECT**](d3d12-rect.md) struttura . |
| [**CD3DX12_RESOURCE_ALLOCATION_INFO**](cd3dx12-resource-allocation-info.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) struttura . |
| [**CD3DX12_RESOURCE_BARRIER**](cd3dx12-resource-barrier.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_RESOURCE_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier) struttura . |
| [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_RESOURCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc) struttura . |
| [**CD3DX12_RESOURCE_DESC1**](cd3dx12-resource-desc1.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) struttura . |
| [**CD3DX12_ROOT_CONSTANTS**](cd3dx12-root-constants.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_ROOT_CONSTANTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_constants) struttura . |
| [**CD3DX12_ROOT_DESCRIPTOR**](cd3dx12-root-descriptor.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_ROOT_DESCRIPTOR**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor) struttura . |
| [**CD3DX12_ROOT_DESCRIPTOR1**](cd3dx12-root-descriptor1.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_ROOT_DESCRIPTOR1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor1) struttura . |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE**](cd3dx12-root-descriptor-table.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) struttura . |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE1**](cd3dx12-root-descriptor-table1.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) struttura . |
| [**CD3DX12_ROOT_PARAMETER**](cd3dx12-root-parameter.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_ROOT_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter) struttura . |
| [**CD3DX12_ROOT_PARAMETER1**](cd3dx12-root-parameter1.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_ROOT_PARAMETER1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter1) struttura . |
| [**CD3DX12_ROOT_SIGNATURE_DESC**](cd3dx12-root-signature-desc.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) struttura . |
| [**CD3DX12_RT_FORMAT_ARRAY**](cd3dx12-rt-format-array.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_RT_FORMAT_ARRAY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rt_format_array) struttura . |
| [**CD3DX12_SHADER_BYTECODE**](cd3dx12-shader-bytecode.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_SHADER_BYTECODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode) struttura . |
| [**CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT**](cd3dx12-state-object-config-subobject.md) | Classe helper per la creazione di un oggetto secondario che definisce le proprietà generali di un oggetto di stato. |
| [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) | Classe centrale degli helper di creazione di oggetti di stato D3DX12, che sono classi helper per la creazione di oggetti di stato da un set arbitrario di oggetti secondari. |
| [**CD3DX12_STATIC_SAMPLER_DESC**](cd3dx12-static-sampler-desc.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_STATIC_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) struttura . |
| [**CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT**](cd3dx12-subobject-to-exports-association-subobject.md) | Classe helper per la creazione di un oggetto secondario per esportare un oggetto secondario dello stato di associazione. |
| [**CD3DX12_SUBRESOURCE_FOOTPRINT**](cd3dx12-subresource-footprint.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_footprint) struttura . |
| [**CD3DX12_SUBRESOURCE_RANGE_UINT64**](cd3dx12-subresource-range-uint64.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) struttura . |
| [**CD3DX12_SUBRESOURCE_TILING**](cd3dx12-subresource-tiling.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_SUBRESOURCE_TILING**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_tiling) struttura . |
| [**CD3DX12_TEXTURE_COPY_LOCATION**](cd3dx12-texture-copy-location.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_TEXTURE_COPY_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texture_copy_location) struttura . |
| [**CD3DX12_TILE_REGION_SIZE**](cd3dx12-tile-region-size.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) struttura . |
| [**CD3DX12_TILE_SHAPE**](cd3dx12-tile-shape.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) struttura . |
| [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) struttura . |
| [**CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC**](cd3dx12-versioned-root-signature-desc.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) struttura . |
| [**CD3DX12_VIEW_INSTANCING_DESC**](cd3dx12-view-instancing-desc.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) struttura . |
| [**CD3DX12_VIEWPORT**](cd3dx12-viewport.md) | Struttura helper per consentire un'inizializzazione semplice di una [**D3D12_VIEWPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport) struttura . |
| [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) | Per [gli shader mesh/amplifications,](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html)è possibile usare i dati di [un effectPipelineStateDescription](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription), **con D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**, per fornire tutto lo stato. |

## <a name="related-topics"></a>Argomenti correlati

* [Strutture e funzioni helper per D3D12](helper-structures-and-functions-for-d3d12.md)
* [Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
