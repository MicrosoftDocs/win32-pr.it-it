---
title: Strutture di base (grafica Direct3D 12)
description: Le strutture seguenti sono dichiarate in d3d12. h.
ms.assetid: 7FE8796A-98D1-4333-8755-2A47567460B3
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 456ca501426142182d9823427c7d13599e4a92db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300354"
---
# <a name="core-structures"></a>Strutture di base

Le strutture seguenti sono dichiarate in d3d12. h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento e descrizione |
|-|
| [**D3D12_AUTO_BREADCRUMB_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node). Rappresenta i dati di navigazione automatica dei dati estesi (eseguire) rimossi dal dispositivo come nodo in un elenco collegato. |
| [**D3D12_BLEND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc). Descrive lo stato di Blend. |
| [**D3D12_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box). Descrive una casella 3D. |
| [**D3D12_BUFFER_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_rtv). Descrive gli elementi di una risorsa buffer da utilizzare in una visualizzazione di destinazione di rendering. |
| [**D3D12_BUFFER_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv). Descrive gli elementi in una risorsa di buffer da usare in una visualizzazione risorse dello shader. |
| [**D3D12_BUFFER_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav). Descrive gli elementi di un buffer da utilizzare in una visualizzazione di accesso non ordinato. |
| [**D3D12_CACHED_PIPELINE_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state). Archivia uno stato della pipeline. |
| [**D3D12_CLEAR_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value). Descrive un valore usato per ottimizzare le operazioni di cancellazione per una determinata risorsa. |
| [**D3D12_COMMAND_QUEUE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_queue_desc). Descrive una coda di comandi. |
| [**D3D12_COMMAND_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Descrive gli argomenti (parametri) della firma di un comando. |
| [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). Descrive un oggetto di stato della pipeline di calcolo. |
| [**D3D12_CONSTANT_BUFFER_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc). Descrive un buffer costante da visualizzare. |
| [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle). Descrive un handle del descrittore della CPU. |
| [**D3D12_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc). Descrive lo stato di depth-stencil. |
| [**D3D12_DEPTH_STENCIL_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1). Descrive lo stato di depth-stencil. |
| [**D3D12_DEPTH_STENCIL_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_value). Specifica un valore di profondità e stencil. |
| [**D3D12_DEPTH_STENCIL_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc). Descrive le sottorisorse di una trama a cui è possibile accedere da una visualizzazione di stencil profondità. |
| [**D3D12_DEPTH_STENCILOP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc). Descrive le operazioni dello stencil che possono essere eseguite in base ai risultati del test dello stencil. |
| [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc). Descrive l'heap del descrittore. |
| [**D3D12_DESCRIPTOR_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range). Descrive un intervallo di descrittori. |
| [**D3D12_DESCRIPTOR_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1). Descrive un intervallo di descrittori con i flag per determinare la loro volatilità. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data). Rappresenta i dati della versione 1,0 dei dati estesi rimossi del dispositivo (eseguire). |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data1). Rappresenta i dati di rimozione del dispositivo rimossi (eseguire) della versione 1,1 del dispositivo, in modo che i debugger e le estensioni del debugger possano accedere ai dati di eseguire. |
| [**D3D12_DISCARD_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region). Descrive i dettagli dell'operazione di eliminazione delle risorse. |
| [**D3D12_DISPATCH_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments). Descrive i parametri di invio per l'uso da parte del compute shader. |
| [**D3D12_DRAW_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments). Descrive i parametri per la creazione di istanze. |
| [**D3D12_DRAW_INDEXED_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments). Descrive i parametri per il disegno di istanze indicizzate. |
| [**D3D12_DRED_ALLOCATION_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_allocation_node). Descrive, come nodo in un elenco collegato, i dati relativi a un'allocazione rilevata dal dispositivo rimossi dati estesi (eseguire). |
| [**D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_auto_breadcrumbs_output). Contiene un puntatore all'inizio di un elenco collegato di oggetti [D3D12_AUTO_BREADCRUMB_NODE](/windows/desktop/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node) . L'elenco rappresenta lo stato di navigazione automatica prima della rimozione del dispositivo. |
| [**D3D12_DRED_PAGE_FAULT_OUTPUT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_page_fault_output). Descrive i dati di allocazione correlati a un errore di pagina GPU in un indirizzo virtuale specificato (VA). |
| [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture). Fornire informazioni dettagliate sull'architettura dell'adapter, aiutando le applicazioni a ottimizzare le prestazioni per determinate proprietà dell'adapter. |
| [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1). Fornire informazioni dettagliate sull'architettura dell'adapter, aiutando le applicazioni a ottimizzare le prestazioni per determinate proprietà dell'adapter. |
| [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority). Viene dettagliatamente il supporto dell'adapter per la definizione delle priorità di diversi tipi di coda dei comandi. |
| [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node). Indica il livello di supporto per la condivisione di risorse tra diversi adapter. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). Descrive le opzioni della funzionalità Direct3D 12 nel driver di grafica corrente. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1). Descrive il livello di supporto per le operazioni HLSL 6,0 Wave. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2). Informazioni dettagliate sul supporto dell'adapter per alcune funzionalità facoltative di Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3). Utilizzato per indicare il livello di supporto fornito dall'adapter per le funzionalità facoltative di Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4). Indica il livello di supporto per trame MSAA allineate a 64KB, condivisione tra API e operazioni shader a 16 bit native. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5). Indica il livello di supporto fornito dall'adapter per le risorse di rendering, il servizio di traccia e il livello 3 di visualizzazione delle risorse. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6). Indica il livello di supporto fornito dall'adapter per l'ombreggiatura a frequenza variabile (VRS) e indica se è supportata l'elaborazione in background. |
| [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps). Utilizzato per determinare se l'adapter supporta la creazione di heap dalla memoria di sistema esistente. Tali heap non sono destinati all'uso generale, ma sono particolarmente utili per scopi diagnostici, in quanto è garantita la permanenza anche dopo gli errori dell'adapter o l'esperienza di un evento di rimozione del dispositivo. |
| [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels). Descrive le informazioni sui [livelli di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supportati dal driver grafico corrente. |
| [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info). Descrive il formato dati DXGI. |
| [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support). Descrive le risorse supportate dal driver grafico corrente per un determinato formato. |
| [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support). Descrive le limitazioni dello spazio degli indirizzi virtuali della GPU dell'adapter, inclusi i bit di indirizzo massimo per risorsa e per processo. |
| [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels). Descrive i livelli di qualità dell'immagine per un determinato formato e un numero di campioni. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support). Indica il livello di supporto per le sessioni di risorse protette. |
| [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command). Indica il livello di supporto fornito dall'adapter per i metacomandi. |
| [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature). Passare questa struttura a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) per verificare il supporto della versione della firma radice. |
| [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization). Indica il livello di supporto per la serializzazione dell'heap. |
| [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache). Descrive il livello di memorizzazione nella cache dello shader supportato nel driver grafico corrente. |
| [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model). Contiene il modello di shader supportato. |
| [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle). Descrive un handle del descrittore della GPU. |
| [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc). Descrive un oggetto di stato della pipeline grafica. |
| [**D3D12_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc). Descrive un heap. |
| [**D3D12_HEAP_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties). Descrive le proprietà dell'heap. |
| [**D3D12_INDEX_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view). Descrive il buffer di indice da visualizzare. |
| [**D3D12_INDIRECT_ARGUMENT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc). Descrive un argomento indiretto (un parametro indiretto), da utilizzare con una firma del comando. |
| [**D3D12_INPUT_ELEMENT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_element_desc). Descrive un singolo elemento per la fase input-assembler della pipeline grafica. |
| [**D3D12_INPUT_LAYOUT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc). Descrive i dati del buffer di input per la fase input-assembler. |
| [**D3D12_MEMCPY_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest). Descrive la destinazione di un'operazione di copia della memoria. |
| [**D3D12_META_COMMAND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_meta_command_desc). Descrive un meta Command. |
| [**D3D12_META_COMMAND_PARAMETER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_meta_command_parameter_desc). Descrive un parametro per un meta Command. |
| [**D3D12_PACKED_MIP_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info). Descrive la struttura dei riquadri di una risorsa affiancata con mipmap. |
| [**D3D12_PIPELINE_STATE_STREAM_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc). Descrive un flusso di stato della pipeline. |
| [**D3D12_PLACED_SUBRESOURCE_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint). Descrive il footprint di una sottorisorsa posizionata, inclusi l'offset e la D3D12_SUBRESOURCE_FOOTPRINT. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_protected_resource_session_desc). Descrive i flag per una sessione di risorse protette, per scheda. |
| [**D3D12_QUERY_DATA_PIPELINE_STATISTICS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_data_pipeline_statistics). Eseguire query sulle informazioni sulle attività della pipeline grafica tra le chiamate a [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery). |
| [**D3D12_QUERY_DATA_SO_STATISTICS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_data_so_statistics). Descrive i dati di query per l'output del flusso. |
| [**D3D12_QUERY_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc). Descrive lo scopo di un heap di query. Un heap di query contiene una matrice di singole query. |
| [**D3D12_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range). Descrive un intervallo di memoria. |
| [**D3D12_RANGE_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64). Descrive un intervallo di memoria in uno spazio degli indirizzi a 64 bit. |
| [**D3D12_RASTERIZER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc). Descrive lo stato di rasterizzazione. |
| [**D3D12_RAYTRACING_AABB**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_aabb). Rappresenta un rettangolo di delimitazione allineato all'asse (AABB) utilizzato come raytracing Geometry. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_compacted_size_desc). Descrive il requisito di spazio per la struttura di accelerazione dopo la compattazione. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_current_size_desc). Descrive lo spazio attualmente utilizzato da una struttura di accelerazione. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_desc). Descrizione delle informazioni di post-compilazione da generare da una struttura di accelerazione. Usare questa struttura nelle chiamate a [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) e [**BuildRaytracingAccelerationStructure**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc). Descrive le dimensioni e il layout della struttura e dell'intestazione di accelerazione serializzata |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_tools_visualization_desc). Viene descritto il requisito di spazio per la decodifica di una struttura di accelerazione in un modulo che può essere visualizzato da strumenti. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_prebuild_info). Rappresenta le informazioni sulla precompilazione di una struttura di accelerazione raytracing. Ottenere un'istanza di questo struttura chiamando [**GetRaytracingAccelerationStructurePrebuildInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv). Struttura di visualizzazione delle risorse dello shader (SRV) per l'archiviazione di una struttura di accelerazione raytracing. |
| [**D3D12_RAYTRACING_GEOMETRY_AABBS_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc). Descrive un set di caselle di delimitazione allineate all'asse utilizzate nella struttura [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) per fornire dati di input a un'operazione di compilazione della struttura di accelerazione RAYTRACING. |
| [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). Descrive un set di geometria usato nella struttura di [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) per fornire i dati di input a un'operazione di compilazione della struttura di accelerazione RAYTRACING. |
| [**D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc). Descrive un set di triangoli usati come geometria raytracing. La geometria a cui fa riferimento questo struct è sempre in formato elenco triangolo, indicizzata o non indicizzata. Le strisce triangolari non sono supportate. |
| [**D3D12_RAYTRACING_INSTANCE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_instance_desc). Descrive un'istanza di una struttura di accelerazione raytracing utilizzata nella memoria GPU durante il processo di compilazione della struttura di accelerazione. |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config). Sottooggetto di stato che rappresenta una configurazione della pipeline raytracing. |
| [**D3D12_RAYTRACING_SHADER_CONFIG**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config). Sottooggetto di stato che rappresenta una configurazione dello shader. |
| [**D3D12_RECT**](d3d12-rect.md). D3D12_RECT viene dichiarata come RECT. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access). Descrive l'accesso alle risorse richieste da un'applicazione in fase di transizione in un passaggio di rendering. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_CLEAR_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access_clear_parameters). Descrive il valore non crittografato al quale le risorse devono essere cancellate all'inizio di un passaggio di rendering. |
| [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc). Descrive un'associazione (fissa per la durata del passaggio di rendering) a una vista depth stencil (DSV), nonché alle caratteristiche di accesso iniziale e finale. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access). Descrive l'accesso alle risorse richieste da un'applicazione in fase di transizione da un passaggio di rendering. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_parameters). Descrive una risorsa da risolvere in al termine di un passaggio di rendering. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_subresource_parameters). Descrive le sottorisorse necessarie per la risoluzione al termine di un passaggio di rendering. |
| [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc). Descrive i binding (corretti per la durata del passaggio di rendering) a una o più visualizzazioni di destinazione di rendering (RTVs), nonché le caratteristiche di accesso iniziale e finale. |
| [**D3D12_RENDER_TARGET_BLEND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc). Descrive lo stato di Blend per una destinazione di rendering. |
| [**D3D12_RENDER_TARGET_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc). Descrive le sottorisorse di una risorsa accessibile tramite una visualizzazione di destinazione del rendering. |
| [**D3D12_RESOURCE_ALIASING_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier). Descrive la transizione tra gli utilizzi di due diverse risorse che hanno mapping nello stesso heap. |
| [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info). Descrive i parametri necessari per allocare le risorse. |
| [**D3D12_RESOURCE_ALLOCATION_INFO1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info1). Descrive i parametri necessari per allocare le risorse, incluso l'offset. |
| [**D3D12_RESOURCE_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier). Descrive una barriera delle risorse (transizione nell'uso delle risorse). |
| [**D3D12_RESOURCE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc). Descrive una risorsa, ad esempio una trama. Questa struttura viene utilizzata ampiamente. |
| [**D3D12_RESOURCE_TRANSITION_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier). Descrive la transizione delle sottorisorse tra diversi utilizzi. |
| [**D3D12_RESOURCE_UAV_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier). Rappresenta una risorsa in cui tutti gli accessi UAV devono essere completati prima che possano iniziare gli accessi UAV futuri. |
| [**D3D12_ROOT_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants). Descrive le costanti inline nella firma radice visualizzate negli shader come un buffer costante. |
| [**D3D12_ROOT_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor). Descrive i descrittori incorporati nella firma radice versione 1,0 visualizzata in shader. |
| [**D3D12_ROOT_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1). Descrive i descrittori incorporati nella firma radice versione 1,1 visualizzata in shader. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table). Descrive il layout della firma radice 1,0 di una tabella dei descrittori come una raccolta di intervalli di descrittori che vengono visualizzati uno dopo l'altro in un heap del descrittore. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1). Descrive il layout della firma radice 1,1 di una tabella dei descrittori come una raccolta di intervalli di descrittori che vengono visualizzati uno dopo l'altro in un heap del descrittore. |
| [**D3D12_ROOT_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter). Descrive lo slot di una firma radice versione 1,0. |
| [**D3D12_ROOT_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1). Descrive lo slot di una firma radice versione 1,1. |
| [**D3D12_ROOT_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc). Descrive il layout di una firma radice versione 1,0. |
| [**D3D12_ROOT_SIGNATURE_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1). Descrive il layout di una firma radice versione 1,1. |
| [**D3D12_RT_FORMAT_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array). Esegue il wrapping di una matrice di formati di destinazione di rendering. |
| [**D3D12_SAMPLE_POSITION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sample_position). Descrive una posizione di esempio di un sottopixel da usare con le posizioni di esempio programmabili. |
| [**D3D12_SAMPLER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc). Descrive uno stato del campionatore. |
| [**D3D12_SHADER_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode). Descrive i dati dello shader. |
| [**D3D12_SHADER_RESOURCE_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc). Descrive una visualizzazione delle risorse dello shader. |
| [**D3D12_SO_DECLARATION_ENTRY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_so_declaration_entry). Descrive un elemento vertice in un buffer vertex in uno slot di output. |
| [**D3D12_STATIC_SAMPLER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc). Descrive un campionatore statico. |
| [**D3D12_STREAM_OUTPUT_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_buffer_view). Descrive un buffer di output del flusso. |
| [**D3D12_STREAM_OUTPUT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc). Descrive un buffer di output del flusso. |
| [**D3D12_SUBRESOURCE_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data). Descrive i dati delle sottorisorse. |
| [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint). Descrive il formato, la larghezza, l'altezza, la profondità e il pitch di riga della sottorisorsa nella risorsa padre. |
| [**D3D12_SUBRESOURCE_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info). Descrive i dati delle sottorisorse. |
| [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64). Descrive un intervallo di memoria della sottorisorsa. |
| [**D3D12_SUBRESOURCE_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling). Descrive un volume di sottorisorse affiancato. |
| [**D3D12_TEX1D_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv). Descrive le sottorisorse di una matrice di trame 1D da usare in una visualizzazione di stencil di profondità. |
| [**D3D12_TEX1D_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv). Descrive le sottorisorse di una matrice di trame 1D da usare in una visualizzazione di destinazione di rendering. |
| [**D3D12_TEX1D_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv). Descrive le sottorisorse di una matrice di trame 1D da usare in una visualizzazione risorse shader. |
| [**D3D12_TEX1D_ARRAY_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav). Descrive una matrice di risorse di trama 1D con accesso non ordinato. |
| [**D3D12_TEX1D_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv). Descrive la sottorisorsa da una trama 1D accessibile a una visualizzazione di stencil di profondità. |
| [**D3D12_TEX1D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv). Descrive la sottorisorsa da una trama 1D da usare in una visualizzazione di destinazione di rendering. |
| [**D3D12_TEX1D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv). Specifica la sottorisorsa da una trama 1D da usare in una visualizzazione risorse dello shader. |
| [**D3D12_TEX1D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav). Descrive una risorsa di trama 1D con accesso non ordinato. |
| [**D3D12_TEX2D_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv). Descrive le sottorisorse di una matrice di trame 2D accessibili a una visualizzazione di stencil di profondità. |
| [**D3D12_TEX2D_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv). Descrive le sottorisorse di una matrice di trame 2D da usare in una visualizzazione di destinazione del rendering. |
| [**D3D12_TEX2D_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv). Descrive le sottorisorse di una matrice di trame 2D da usare in una visualizzazione risorse shader. |
| [**D3D12_TEX2D_ARRAY_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav). Descrive una matrice di risorse di trama 2D con accesso non ordinato. |
| [**D3D12_TEX2D_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv). Descrive la sottorisorsa da una trama 2D accessibile a una visualizzazione di stencil di profondità. |
| [**D3D12_TEX2D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv). Descrive la sottorisorsa da una trama 2D da usare in una visualizzazione di destinazione di rendering. |
| [**D3D12_TEX2D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv). Descrive la sottorisorsa da una trama 2D da usare in una visualizzazione risorse shader. |
| [**D3D12_TEX2D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav). Descrive una risorsa di trama 2D con accesso non ordinato. |
| [**D3D12_TEX2DMS_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv). Descrive le sottorisorse di una matrice di trame 2D multicampionate per una visualizzazione con stencil di profondità. |
| [**D3D12_TEX2DMS_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv). Descrive le sottorisorse di una matrice di trame 2D multicampionate da usare in una visualizzazione di destinazione di rendering. |
| [**D3D12_TEX2DMS_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv). Descrive le sottorisorse di una matrice di trame 2D multicampionate da usare in una visualizzazione delle risorse dello shader. |
| [**D3D12_TEX2DMS_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv). Descrive la sottorisorsa da una trama 2D multicampionata accessibile a una visualizzazione di stencil di profondità. |
| [**D3D12_TEX2DMS_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv). Descrive la sottorisorsa da una trama 2D multicampionata da usare in una visualizzazione di destinazione di rendering. |
| [**D3D12_TEX2DMS_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_srv). Descrive le sottorisorse da una trama 2D multicampionata da usare in una visualizzazione risorse shader. |
| [**D3D12_TEX3D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv). Descrive le sottorisorse di una trama 3D da usare in una visualizzazione di destinazione del rendering. |
| [**D3D12_TEX3D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_srv). Descrive le sottorisorse di una trama 3D da usare in una visualizzazione risorse dello shader. |
| [**D3D12_TEX3D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav). Descrive una risorsa di trama 3D con accesso non ordinato. |
| [**D3D12_TEXCUBE_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_array_srv). Descrive le sottorisorse di una matrice di trame del cubo da usare in una visualizzazione risorse shader. |
| [**D3D12_TEXCUBE_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_srv). Descrive la sottorisorsa da una trama del cubo da usare in una visualizzazione risorse dello shader. |
| [**D3D12_TEXTURE_COPY_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location). Descrive una parte di una trama per lo scopo delle copie di trama. |
| [**D3D12_TILE_REGION_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size). Descrive le dimensioni di un'area affiancata. |
| [**D3D12_TILE_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape). Descrive la forma di un riquadro specificandone le dimensioni. |
| [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate). Descrive le coordinate di una risorsa affiancata. |
| [**D3D12_UNORDERED_ACCESS_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc). Descrive le sottorisorse di una risorsa accessibile tramite una visualizzazione di accesso non ordinato. |
| [**D3D12_VERTEX_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view). Descrive una visualizzazione del buffer dei vertici. |
| [**D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). Rappresenta il dispositivo con versione rimossi dati estesi (eseguire), in modo che i debugger e le estensioni del debugger possano accedere ai dati di eseguire. |
| [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc). Contiene una versione di una descrizione della firma radice ed è progettata per essere utilizzata con funzioni di serializzazione/deserializzazione. |
| [**D3D12_VIEW_INSTANCE_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_view_instance_location). Specifica il viewport/stencil e la destinazione di rendering associati a un'istanza di visualizzazione. |
| [**D3D12_VIEW_INSTANCING_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_view_instancing_desc). Specifica i parametri utilizzati durante la configurazione delle istanze di visualizzazione. |
| [**D3D12_VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport). Descrive le dimensioni di un viewport. |
| [**D3D12_WRITEBUFFERIMMEDIATE_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_writebufferimmediate_parameter). Specifica il valore immediato e l'indirizzo di destinazione scritti con [**ID3D12CommandList2:: WriteBufferImmediate**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2). |

## <a name="related-topics"></a>Argomenti correlati

* [Riferimento principale](direct3d-12-core-reference.md)
* [Guida di riferimento a Direct3D 12](direct3d-12-reference.md)