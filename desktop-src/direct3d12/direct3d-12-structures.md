---
title: Strutture di base (grafica Direct3D 12)
description: Le strutture seguenti sono dichiarate in d3d12.h.
ms.assetid: 7FE8796A-98D1-4333-8755-2A47567460B3
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 4222e9637d87f5c2a6df7a296465c8b9d148dde87a6698f8296fb0a1ed646345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608551"
---
# <a name="core-structures"></a>Strutture di base

Le strutture seguenti sono dichiarate in d3d12.h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento e descrizione |
|-|
| [**D3D12_AUTO_BREADCRUMB_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node). Rappresenta i dati di navigazione automatica DRED (Device Removed Extended Data) come nodo in un elenco collegato. |
| [**D3D12_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc). Descrive lo stato di fusione. |
| [**D3D12_BOX**](/windows/win32/api/d3d12/ns-d3d12-d3d12_box). Descrive una casella 3D. |
| [**D3D12_BUFFER_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_rtv). Descrive gli elementi in una risorsa buffer da usare in una visualizzazione di destinazione di rendering. |
| [**D3D12_BUFFER_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_srv). Descrive gli elementi in una risorsa buffer da usare in una visualizzazione shader-risorsa. |
| [**D3D12_BUFFER_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_uav). Descrive gli elementi in un buffer da utilizzare in una visualizzazione di accesso non ordinato. |
| [**D3D12_CACHED_PIPELINE_STATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state). Archivia uno stato della pipeline. |
| [**D3D12_CLEAR_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value). Descrive un valore utilizzato per ottimizzare le operazioni di cancellazione per una determinata risorsa. |
| [**D3D12_COMMAND_QUEUE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc). Descrive una coda di comandi. |
| [**D3D12_COMMAND_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Descrive gli argomenti (parametri) di una firma di comando. |
| [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). Descrive un oggetto stato della pipeline di calcolo. |
| [**D3D12_CONSTANT_BUFFER_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc). Descrive un buffer costante da visualizzare. |
| [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle). Descrive un handle del descrittore della CPU. |
| [**D3D12_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc). Descrive lo stato depth-stencil. |
| [**D3D12_DEPTH_STENCIL_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1). Descrive lo stato depth-stencil. |
| [**D3D12_DEPTH_STENCIL_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_value). Specifica una profondità e un valore di stencil. |
| [**D3D12_DEPTH_STENCIL_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc). Descrive le sottorisorse di una trama accessibili da una visualizzazione depth-stencil. |
| [**D3D12_DEPTH_STENCILOP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc). Descrive le operazioni di stencil che possono essere eseguite in base ai risultati del test di stencil. |
| [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc). Descrive l'heap del descrittore. |
| [**D3D12_DESCRIPTOR_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range). Descrive un intervallo di descrittori. |
| [**D3D12_DESCRIPTOR_RANGE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range1). Descrive un intervallo di descrittori, con flag per determinarne la volatilità. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data). Rappresenta i dati drED (Device Removed Extended Data) versione 1.0. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data1). Rappresenta i dati di rimozione dei dispositivi drED (Device Removed Extended Data) versione 1.1, in modo che i debugger e le estensioni del debugger possano accedere ai dati DRED. |
| [**D3D12_DISCARD_REGION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_discard_region). Descrive i dettagli per l'operazione discard-resource. |
| [**D3D12_DISPATCH_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dispatch_arguments). Descrive i parametri di invio, per l'uso da parte dello shader di calcolo. |
| [**D3D12_DRAW_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_draw_arguments). Descrive i parametri per le istanze di disegno. |
| [**D3D12_DRAW_INDEXED_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments). Descrive i parametri per il disegno di istanze indicizzate. |
| [**D3D12_DRED_ALLOCATION_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_allocation_node). Descrive, come nodo in un elenco collegato, i dati relativi a un'allocazione rilevata da Device Removed Extended Data (DRED). |
| [**D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_auto_breadcrumbs_output). Contiene un puntatore all'inizio di un elenco collegato [di D3D12_AUTO_BREADCRUMB_NODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node) oggetti . L'elenco rappresenta lo stato di navigazione automatica prima della rimozione del dispositivo. |
| [**D3D12_DRED_PAGE_FAULT_OUTPUT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_page_fault_output). Descrive i dati di allocazione correlati a un errore di pagina GPU in un determinato indirizzo virtuale (VA). |
| [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture). Fornire informazioni dettagliate sull'architettura dell'adapter, consentendo alle applicazioni di ottimizzare meglio determinate proprietà dell'adapter. |
| [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1). Fornire informazioni dettagliate sull'architettura dell'adapter, consentendo alle applicazioni di ottimizzare meglio determinate proprietà dell'adapter. |
| [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority). Informazioni dettagliate sul supporto dell'adapter per la definizione delle priorità dei diversi tipi di code di comandi. |
| [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node). Indica il livello di supporto per la condivisione di risorse tra schede diverse. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). Descrive le opzioni delle funzionalità direct3D 12 nel driver di grafica corrente. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1). Descrive il livello di supporto per le operazioni wave HLSL 6.0. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2). Informazioni dettagliate sul supporto dell'adapter per alcune funzionalità facoltative di Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3). Usato per indicare il livello di supporto fornito dall'adapter per le funzionalità facoltative di Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4). Indica il livello di supporto per trame MSAA allineate a 64 KB, condivisione tra API e operazioni shader native a 16 bit. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5). Indica il livello di supporto fornito dall'adattatore per i passaggi di rendering, la traccia dei raggi e le risorse affiancate di livello 3 della visualizzazione di risorse shader. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6). Indica il livello di supporto fornito dall'adattatore per l'ombreggiatura a velocità variabile e indica se è supportata o meno l'elaborazione in background. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS7**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options7). Indica il livello di supporto fornito dall'adattatore per gli shader mesh e di amplificazione e per il feedback del campionatore. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS8**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options8). Indica se sono supportate o meno trame non allineate compresse a blocchi. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS9**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9). Indica se esiste o meno il supporto per gli shader mesh, i valori di SV_RenderTargetArrayIndex che sono 8 o *superiori,* atomici di interi a 64 bit di risorsa tipidata, operazioni di esempio di trama derivata e dipendente da derivati e il livello di supporto per le operazioni WaveMMA (wave_matrix). |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS10**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options10). Indica se è possibile usare o meno il combinatore SUM e se è possibile SV_ShadingRate da uno shader mesh.  |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS11**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options11). Indica se sono supportati o meno atomici interi a 64 bit nelle risorse negli heap dei descrittori. |
| [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps). Utilizzato per determinare se l'adattatore supporta la creazione di heap dalla memoria di sistema esistente. Questi heap non sono destinati all'uso generale, ma sono estremamente utili a scopo diagnostico perché sono garantiti per la persistenza anche dopo gli errori dell'adattatore o quando si verifica un evento di rimozione del dispositivo. |
| [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels). Descrive le informazioni sui [livelli di funzionalità](/windows/win32/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supportati dal driver di grafica corrente. |
| [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_format_info). Descrive il formato dati DXGI. |
| [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_format_support). Descrive le risorse supportate dal driver di grafica corrente per un formato specificato. |
| [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support). Informazioni dettagliate sulle limitazioni dello spazio degli indirizzi virtuali GPU della scheda, inclusi i bit di indirizzo massimi per risorsa e per processo. |
| [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels). Descrive i livelli di qualità delle immagini per un formato e un numero di campioni specificato. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support). Indica il livello di supporto per le sessioni di risorse protette. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPE_COUNT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_type_count). Indica un conteggio dei tipi di sessione di risorse protette. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_types). Indica un elenco di tipi di sessione di risorse protette. |
| [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command). Indica il livello di supporto fornito dall'adattatore per i metacomandi. |
| [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature). Passare questa struttura a [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) per verificare il supporto della versione della firma radice. |
| [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_serialization). Indica il livello di supporto per la serializzazione dell'heap. |
| [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache). Descrive il livello di memorizzazione nella cache dello shader supportato nel driver di grafica corrente. |
| [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model). Contiene il modello di shader supportato. |
| [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle). Descrive un handle di descrittore GPU. |
| [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc). Descrive un oggetto stato della pipeline grafica. |
| [**D3D12_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_desc). Descrive un heap. |
| [**D3D12_HEAP_PROPERTIES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties). Vengono descritte le proprietà dell'heap. |
| [**D3D12_INDEX_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_index_buffer_view). Descrive la index buffer da visualizzare. |
| [**D3D12_INDIRECT_ARGUMENT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc). Descrive un argomento indiretto (un parametro indiretto) da usare con una firma di comando. |
| [**D3D12_INPUT_ELEMENT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc). Descrive un singolo elemento per la fase input-assembler della pipeline grafica. |
| [**D3D12_INPUT_LAYOUT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_layout_desc). Descrive i dati del buffer di input per la fase input-assembler. |
| [**D3D12_MEMCPY_DEST**](/windows/win32/api/d3d12/ns-d3d12-d3d12_memcpy_dest). Descrive la destinazione di un'operazione di copia della memoria. |
| [**D3D12_META_COMMAND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_meta_command_desc). Descrive un meta comando. |
| [**D3D12_META_COMMAND_PARAMETER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_meta_command_parameter_desc). Descrive un parametro per un meta comando. |
| [**D3D12_PACKED_MIP_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_packed_mip_info). Descrive la struttura del riquadro di una risorsa affiancata con mipmap. |
| [**D3D12_PIPELINE_STATE_STREAM_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc). Descrive un flusso di stato della pipeline. |
| [**D3D12_PLACED_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint). Descrive il footprint di una sottorisorsa posizionata, inclusi l'offset e la D3D12_SUBRESOURCE_FOOTPRINT. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_protected_resource_session_desc). Descrive i flag per una sessione di risorse protetta, per ogni adapter. |
| [**D3D12_QUERY_DATA_PIPELINE_STATISTICS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_data_pipeline_statistics). Eseguire query sulle informazioni sull'attività della pipeline grafica tra le chiamate [**a BeginQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) [**ed EndQuery.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) |
| [**D3D12_QUERY_DATA_SO_STATISTICS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_data_so_statistics). Descrive i dati di query per l'output del flusso. |
| [**D3D12_QUERY_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc). Descrive lo scopo di un heap di query. Un heap di query contiene una matrice di singole query. |
| [**D3D12_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range). Descrive un intervallo di memoria. |
| [**D3D12_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range_uint64). Descrive un intervallo di memoria in uno spazio indirizzi a 64 bit. |
| [**D3D12_RASTERIZER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc). Descrive lo stato di rasterizzazione. |
| [**D3D12_RAYTRACING_AABB**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_aabb). Rappresenta un rettangolo di selezione allineato all'asse (AABB) utilizzato come geometria di raytracing. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_compacted_size_desc). Descrive il requisito di spazio per la struttura di accelerazione dopo la compattazione. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_current_size_desc). Descrive lo spazio attualmente utilizzato da una struttura di accelerazione. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_desc). Descrizione delle informazioni di post-compilazione da generare da una struttura di accelerazione. Usare questa struttura nelle chiamate [**a EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) [**e BuildRaytracingAccelerationStructure.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure) |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc). Descrive le dimensioni e il layout della struttura e dell'intestazione di accelerazione serializzata |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_tools_visualization_desc). Descrive il requisito di spazio per la decodifica di una struttura di accelerazione in un modulo che può essere visualizzato dagli strumenti. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_prebuild_info). Rappresenta le informazioni di pre-compilazione su una struttura di accelerazione raytracing. Ottenere un'istanza di questo stucture chiamando [**GetRaytracingAccelerationStructurePrebuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv). Struttura di visualizzazione delle risorse shader (SRV) per l'archiviazione di una struttura di accelerazione raytracing. |
| [**D3D12_RAYTRACING_GEOMETRY_AABBS_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc). Descrive un set di rettanci di delimitazione allineati all'asse usati nella [**struttura D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) per fornire dati di input a un'operazione di compilazione della struttura di accelerazione del raggio. |
| [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). Descrive un set di geometria usato nella struttura D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS [**per**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) fornire dati di input a un'operazione di compilazione della struttura di accelerazione raytracing. |
| [**D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc). Descrive un set di triangoli usati come geometria di raytracing. La geometria a cui punta questo struct è sempre in forma di elenco triangolare, indicizzata o non indicizzata. Le strisce triangolare non sono supportate. |
| [**D3D12_RAYTRACING_INSTANCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_instance_desc). Descrive un'istanza di una struttura di accelerazione raytracing usata nella memoria GPU durante il processo di compilazione della struttura di accelerazione. |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config). Oggetto secondario di stato che rappresenta una configurazione della pipeline di raytracing. |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config1). Sottooggetto di stato che rappresenta una configurazione della pipeline di raytracing, con flag. |
| [**D3D12_RAYTRACING_SHADER_CONFIG**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config). Oggetto secondario di stato che rappresenta una configurazione dello shader. |
| [**D3D12_RECT**](d3d12-rect.md). D3D12_RECT viene dichiarato come RECT. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access). Descrive l'accesso alle risorse richieste da un'applicazione durante la transizione a un passaggio di rendering. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_CLEAR_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access_clear_parameters). Descrive il valore non crittografato per cui le risorse devono essere cancellate all'inizio di un passaggio di rendering. |
| [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc). Descrive un'associazione (fissa per la durata del passaggio di rendering) a una vista depth stencil (DSV), nonché le caratteristiche di accesso iniziale e finale. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access). Descrive l'accesso alle risorse richieste da un'applicazione durante la transizione da un passaggio di rendering. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_parameters). Descrive una risorsa in cui risolvere al termine di un passaggio di rendering. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_subresource_parameters). Descrive le sottorisorse coinvolte nella risoluzione al termine di un passaggio di rendering. |
| [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc). Descrive le associazioni (fisse per la durata del passaggio di rendering) a una o più visualizzazioni di destinazione di rendering (RTV), nonché le relative caratteristiche di accesso iniziale e finale. |
| [**D3D12_RENDER_TARGET_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc). Descrive lo stato di blend per una destinazione di rendering. |
| [**D3D12_RENDER_TARGET_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_target_view_desc). Descrive le sottorisorse di una risorsa accessibili tramite una visualizzazione di destinazione di rendering. |
| [**D3D12_RESOURCE_ALIASING_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier). Viene descritta la transizione tra utilizzi di due risorse diverse con mapping nello stesso heap. |
| [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info). Descrive i parametri necessari per allocare risorse. |
| [**D3D12_RESOURCE_ALLOCATION_INFO1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info1). Descrive i parametri necessari per allocare risorse, incluso l'offset. |
| [**D3D12_RESOURCE_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier). Descrive una barriera di risorse (transizione nell'uso delle risorse). |
| [**D3D12_RESOURCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc). Descrive una risorsa, ad esempio una trama. Questa struttura viene ampiamente usata. |
| [**D3D12_RESOURCE_TRANSITION_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier). Descrive la transizione di sottorisorse tra utilizzi diversi. |
| [**D3D12_RESOURCE_UAV_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier). Rappresenta una risorsa in cui tutti gli accessi UAV devono essere completati prima di poter iniziare eventuali accessi UAV futuri. |
| [**D3D12_ROOT_CONSTANTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_constants). Descrive le costanti inline nella firma radice visualizzate negli shader come un buffer costante. |
| [**D3D12_ROOT_DESCRIPTOR**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor). Descrive i descrittori inline nella versione 1.0 della firma radice visualizzati negli shader. |
| [**D3D12_ROOT_DESCRIPTOR1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor1). Descrive i descrittori inline nella versione 1.1 della firma radice visualizzati negli shader. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table). Descrive il layout della firma radice 1.0 di una tabella di descrittori come raccolta di intervalli di descrittori visualizzati uno dopo l'altro in un heap dei descrittori. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1). Descrive il layout della firma radice 1.1 di una tabella di descrittori come raccolta di intervalli di descrittori visualizzati uno dopo l'altro in un heap dei descrittori. |
| [**D3D12_ROOT_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter). Descrive lo slot di una firma radice versione 1.0. |
| [**D3D12_ROOT_PARAMETER1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter1). Descrive lo slot di una firma radice versione 1.1. |
| [**D3D12_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc). Descrive il layout di una firma radice versione 1.0. |
| [**D3D12_ROOT_SIGNATURE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1). Descrive il layout di una firma radice versione 1.1. |
| [**D3D12_RT_FORMAT_ARRAY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rt_format_array). Esegue il wrapping di una matrice di formati di destinazione di rendering. |
| [**D3D12_SAMPLE_POSITION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_sample_position). Descrive una posizione di esempio di sottopixy da usare con posizioni di esempio programmabili. |
| [**D3D12_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_sampler_desc). Descrive uno stato del campionatore. |
| [**D3D12_SHADER_BYTECODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode). Descrive i dati dello shader. |
| [**D3D12_SHADER_CACHE_SESSION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_cache_session_desc). Descrive una sessione della cache shader. |
| [**D3D12_SHADER_RESOURCE_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc). Descrive una visualizzazione shader-risorsa. |
| [**D3D12_SO_DECLARATION_ENTRY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_so_declaration_entry). Descrive un elemento vertice in un buffer dei vertici in uno slot di output. |
| [**D3D12_STATIC_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_static_sampler_desc). Descrive un campionatore statico. |
| [**D3D12_STREAM_OUTPUT_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_stream_output_buffer_view). Descrive un buffer di output del flusso. |
| [**D3D12_STREAM_OUTPUT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_stream_output_desc). Descrive un buffer di output di streaming. |
| [**D3D12_SUBRESOURCE_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_data). Descrive i dati della sottorisorsa. |
| [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_footprint). Descrive il formato, la larghezza, l'altezza, la profondità e il passo di riga della sottorisorsa nella risorsa padre. |
| [**D3D12_SUBRESOURCE_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_info). Descrive i dati della sottorisorsa. |
| [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64). Descrive un intervallo di memoria di sottorisorse. |
| [**D3D12_SUBRESOURCE_TILING**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_tiling). Descrive un volume di sottorisorse affiancate. |
| [**D3D12_TEX1D_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv). Descrive le sottorisorse da una matrice di trame 1D da usare in una visualizzazione depth-stencil. |
| [**D3D12_TEX1D_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv). Descrive le sottorisorse da una matrice di trame 1D da usare in una visualizzazione di destinazione di rendering. |
| [**D3D12_TEX1D_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv). Descrive le sottorisorse da una matrice di trame 1D da usare in una visualizzazione shader-risorsa. |
| [**D3D12_TEX1D_ARRAY_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav). Descrive una matrice di risorse di trama 1D ad accesso non ordinato. |
| [**D3D12_TEX1D_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_dsv). Descrive la sottorisorsa da una trama 1D accessibile a una visualizzazione stencil di profondità. |
| [**D3D12_TEX1D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_rtv). Descrive la sottorisorsa di una trama 1D da usare in una visualizzazione di destinazione di rendering. |
| [**D3D12_TEX1D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_srv). Specifica la sottorisorsa da una trama 1D da usare in una visualizzazione shader-risorsa. |
| [**D3D12_TEX1D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_uav). Descrive una risorsa trama 1D ad accesso non ordinato. |
| [**D3D12_TEX2D_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv). Descrive le sottorisorse da una matrice di trame 2D accessibili a una visualizzazione stencil di profondità. |
| [**D3D12_TEX2D_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv). Descrive le sottorisorse da una matrice di trame 2D da usare in una visualizzazione di destinazione di rendering. |
| [**D3D12_TEX2D_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv). Descrive le sottorisorse di una matrice di trame 2D da usare in una visualizzazione shader-risorsa. |
| [**D3D12_TEX2D_ARRAY_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav). Descrive una matrice di risorse di trama 2D ad accesso non ordinato. |
| [**D3D12_TEX2D_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_dsv). Descrive la sottorisorsa da una trama 2D accessibile a una visualizzazione stencil di profondità. |
| [**D3D12_TEX2D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_rtv). Descrive la sottorisorsa da una trama 2D da usare in una visualizzazione di destinazione di rendering. |
| [**D3D12_TEX2D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_srv). Descrive la sottorisorsa da una trama 2D da usare in una visualizzazione shader-risorsa. |
| [**D3D12_TEX2D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_uav). Descrive una risorsa trama 2D ad accesso non ordinato. |
| [**D3D12_TEX2DMS_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv). Descrive le sottorisorse da una matrice di trame 2D multi-campione per una visualizzazione di stencil di profondità. |
| [**D3D12_TEX2DMS_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv). Descrive le sottorisorse di una matrice di trame 2D multi-campione da usare in una visualizzazione di destinazione di rendering. |
| [**D3D12_TEX2DMS_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv). Descrive le sottorisorse da una matrice di trame 2D multi-campione da usare in una visualizzazione shader-risorsa. |
| [**D3D12_TEX2DMS_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv). Descrive la sottorisorsa da una trama 2D multi campione accessibile a una visualizzazione di stencil di profondità. |
| [**D3D12_TEX2DMS_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv). Descrive la sottorisorsa di una trama 2D multi campione da usare in una visualizzazione di destinazione di rendering. |
| [**D3D12_TEX2DMS_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_srv). Descrive le sottorisorse di una trama 2D multi campione da usare in una visualizzazione shader-risorsa. |
| [**D3D12_TEX3D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_rtv). Descrive le sottorisorse di una trama 3D da usare in una visualizzazione di destinazione di rendering. |
| [**D3D12_TEX3D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_srv). Descrive le sottorisorse di una trama 3D da usare in una visualizzazione shader-risorsa. |
| [**D3D12_TEX3D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_uav). Descrive una risorsa trama 3D ad accesso non ordinato. |
| [**D3D12_TEXCUBE_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texcube_array_srv). Descrive le sottorisorse di una matrice di trame del cubo da usare in una visualizzazione shader-risorsa. |
| [**D3D12_TEXCUBE_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texcube_srv). Descrive la sottorisorsa da una trama del cubo da usare in una visualizzazione shader-risorsa. |
| [**D3D12_TEXTURE_COPY_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texture_copy_location). Descrive una parte di una trama ai fini delle copie della trama. |
| [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size). Descrive le dimensioni di un'area affiancata. |
| [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape). Descrive la forma di un riquadro specificandone le dimensioni. |
| [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate). Descrive le coordinate di una risorsa affiancata. |
| [**D3D12_UNORDERED_ACCESS_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc). Descrive le sottorisorse di una risorsa accessibili tramite una visualizzazione di accesso non ordinato. |
| [**D3D12_VERTEX_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view). Descrive una visualizzazione vertex buffer. |
| [**D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). Rappresenta i dati DRED (Device Removed Extended Data) con controllo delle versioni, in modo che i debugger e le estensioni del debugger possano accedere ai dati DRED. |
| [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc). Contiene qualsiasi versione di una descrizione della firma radice ed è progettato per essere utilizzato con le funzioni di serializzazione/deserializzazione. |
| [**D3D12_VIEW_INSTANCE_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instance_location). Specifica il viewport/stencil e la destinazione di rendering associati a un'istanza di visualizzazione. |
| [**D3D12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc). Specifica i parametri utilizzati durante la configurazione delle istanze di visualizzazione. |
| [**D3D12_VIEWPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport). Descrive le dimensioni di un viewport. |
| [**D3D12_WRITEBUFFERIMMEDIATE_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_writebufferimmediate_parameter). Specifica il valore immediato e l'indirizzo di destinazione scritti [**usando ID3D12CommandList2::WriteBufferImmediate.**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) |

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni di riferimento di base](direct3d-12-core-reference.md)
* [Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)