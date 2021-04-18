---
title: Enumerazioni di base
description: Le enumerazioni seguenti sono dichiarate in d3d12. h.
ms.assetid: 76E76C85-128E-4F0E-9711-C72C4CF6C835
ms.localizationpriority: low
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 7f34266e4afdec14e97caa81f393733f1c1ec684
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "106300678"
---
# <a name="core-enumerations"></a>Enumerazioni di base

Le enumerazioni seguenti sono dichiarate in d3d12. h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento e descrizione |
|-|
| [**D3D_ROOT_SIGNATURE_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version). Specifica la versione del layout della firma radice. |
| [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model). Specifica un modello di shader. |
| [**D3D12_AUTO_BREADCRUMB_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_auto_breadcrumb_op). Definisce le costanti che specificano le operazioni di rendering/calcolo della GPU. |
| [**D3D12_BACKGROUND_PROCESSING_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_background_processing_mode). Definisce le costanti che specificano un livello di ottimizzazione dinamica da applicare al lavoro GPU inviato successivamente. |
| [**D3D12_BLEND**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend). Specifica i fattori di Blend, che modulano i valori per il pixel shader e la destinazione di rendering. |
| [**D3D12_BLEND_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend_op). Specifica le operazioni di fusione RGB o Alpha. |
| [**D3D12_BUFFER_SRV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags). Identifica la modalità di visualizzazione di una risorsa del buffer. |
| [**D3D12_BUFFER_UAV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags). Identifica le opzioni di visualizzazione di accesso non ordinato per una risorsa del buffer. |
| [**D3D12_CLEAR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_clear_flags). Specifica gli elementi da cancellare dalla visualizzazione depth stencil. |
| [**D3D12_COLOR_WRITE_ENABLE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_color_write_enable). Identifica i componenti di ogni pixel di una destinazione di rendering scrivibile durante la fusione. |
| [**D3D12_COMMAND_LIST_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_support_flags). Utilizzato per determinare quali tipi di elenchi di comandi sono in grado di supportare varie operazioni. |
| [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type). Specifica il tipo di un elenco di comandi. |
| [**D3D12_COMMAND_QUEUE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_flags). Specifica i flag da utilizzare durante la creazione di una coda di comandi. |
| [**D3D12_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_priority). Definisce i livelli di priorità per una coda di comandi. |
| [**D3D12_COMPARISON_FUNC**](/windows/win32/api/d3d12/ne-d3d12-d3d12_comparison_func). Specifica le opzioni di confronto. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode). Indica se la rasterizzazione conservativa è attiva o disattivata. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier). Identifica il livello di rasterizzazione conservativa del livello. |
| [**D3D12_CPU_PAGE_PROPERTY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cpu_page_property). Specifica le proprietà della pagina CPU per l'heap. |
| [**D3D12_CROSS_NODE_SHARING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier). Specifica il livello di condivisione tra i nodi di un adapter, ad esempio il livello 1 emulato, il livello 1 o il livello 2.  |
| [**D3D12_CULL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cull_mode). Specifica che i triangoli con una determinata direzione non vengono disegnati. |
| [**D3D12_DEBUG_DEVICE_PARAMETER_TYPE**](/windows/win32/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type). Specifica il tipo di dati della memoria a cui punta il parametro *pData* di [**ID3D12DebugDevice1:: SetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) e [**ID3D12DebugDevice1:: GetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter). |
| [**D3D12_DEPTH_WRITE_MASK**](/windows/win32/api/d3d12/ne-d3d12-d3d12_depth_write_mask). Identifica la parte di un buffer di stencil Depth per la scrittura di dati di profondità. |
| [**D3D12_DESCRIPTOR_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags). Specifica le opzioni per un heap. |
| [**D3D12_DESCRIPTOR_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type). Specifica un tipo di heap del descrittore.  |
| [**D3D12_DESCRIPTOR_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags). Specifica la volatilità di entrambi i descrittori e i dati a cui fanno riferimento in una descrizione della firma radice 1,1, che può abilitare alcune ottimizzazioni del driver. |
| [**D3D12_DESCRIPTOR_RANGE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type). Specifica un intervallo in modo che, ad esempio, se parte di una tabella del descrittore ha 100 visualizzazioni di risorse shader (SRVs) che l'intervallo può essere dichiarato in una voce anziché 100.  |
| [**D3D12_DRED_ALLOCATION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_allocation_type). Definisce le costanti che specificano le operazioni di rendering/calcolo della GPU. |
| [**D3D12_DRED_ENABLEMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_enablement). Definisce le costanti (usate dall' [interfaccia ID3D12DeviceRemovedExtendedDataSettings](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings)) che specificano come sono abilitate le funzionalità dei dati estesi (eseguire) del dispositivo. |
| [**D3D12_DRED_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_flags). Definisce le costanti utilizzate nella [struttura D3D12_DEVICE_REMOVED_EXTENDED_DATA](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data) per specificare i flag di controllo per il runtime Direct3D. |
| [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version). Definisce le costanti che specificano una versione del dispositivo rimossi dati estesi (eseguire), come usato dalla [struttura D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). |
| [**D3D12_DSV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_dimension). Specifica come accedere a una risorsa utilizzata in una visualizzazione di stencil Depth. |
| [**D3D12_DSV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_flags). Specifica le opzioni di visualizzazione degli stencil di profondità. |
| [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature). Opzioni della funzionalità Direct3D 12 supportate dal driver grafico corrente.  |
| [**D3D12_FENCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Specifica le opzioni di recinzione.  |
| [**D3D12_FILL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fill_mode). Specifica la modalità di riempimento da utilizzare per il rendering di triangoli. |
| [**D3D12_FILTER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter). Specifica le opzioni di filtro durante il campionamento della trama. |
| [**D3D12_FILTER_REDUCTION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_reduction_type). Specifica il tipo di riduzione del filtro.  |
| [**D3D12_FILTER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_type). Specifica il tipo di filtri per l'ingrandimento o il campionatore minification.  |
| [**D3D12_FORMAT_SUPPORT1**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support1). Specifica le risorse supportate per un formato fornito. |
| [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2). Specifica le opzioni di risorse non ordinate supportate per un formato fornito. |
| [**D3D12_GRAPHICS_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_graphics_states). Definisce i flag che specificano gli stati correlati a un elenco di comandi di grafica. I valori possono essere OR bit per bit. |
| [**D3D12_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags). Specifica le opzioni dell'heap, ad esempio se l'heap può contenere trame e se le risorse sono condivise tra gli adapter.  |
| [**D3D12_HEAP_SERIALIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_serialization_tier). Definisce le costanti che specificano il supporto della serializzazione dell'heap. |
| [**D3D12_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type). Specifica il tipo di heap. Quando sono residenti, gli heap si trovano in un pool di memoria fisico specifico con determinate proprietà della cache della CPU.  |
| [**D3D12_INDEX_BUFFER_STRIP_CUT_VALUE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value). Quando si utilizza la topologia di una primitiva a strisce triangolari, le posizioni dei vertici vengono interpretate come vertici di una striscia È presente un valore di indice speciale che rappresenta il desiderio di discontinuità nella striscia, il valore di indice taglia. Questa enumerazione elenca i valori taglia supportati.  |
| [**D3D12_INDIRECT_ARGUMENT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_indirect_argument_type). Specifica il tipo del parametro indiretto.  |
| [**D3D12_INPUT_CLASSIFICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_input_classification). Identifica il tipo di dati contenuti in uno slot di input. |
| [**D3D12_LIFETIME_STATE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_lifetime_state). Definisce le costanti che specificano lo stato di durata di un oggetto con rilevamento della durata. |
| [**D3D12_LOGIC_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_logic_op). Specifica le operazioni logiche da configurare per una destinazione di rendering. |
| [**D3D12_MEASUREMENTS_ACTION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_measurements_action). Definisce le costanti che specificano le operazioni da eseguire con i risultati della strumentazione del carico di lavoro precedente. |
| [**D3D12_MEMORY_POOL**](/windows/win32/api/d3d12/ne-d3d12-d3d12_memory_pool). Specifica il pool di memoria per l'heap. |
| [**D3D12_META_COMMAND_PARAMETER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_flags). Definisce le costanti che specificano i flag per un parametro in un meta Command. I valori possono essere OR bit per bit. |
| [**D3D12_META_COMMAND_PARAMETER_STAGE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_stage). Definisce le costanti che specificano la fase di un parametro per un meta comando. |
| [**D3D12_META_COMMAND_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_type). Definisce le costanti che specificano il tipo di dati di un parametro per un meta comando. |
| [**D3D12_MULTIPLE_FENCE_WAIT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multiple_fence_wait_flags). Specifica più flag di attesa per più recinzioni. |
| [**D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags). Specifica le opzioni per determinare i livelli di qualità.  |
| [**D3D12_PIPELINE_STATE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags). Flag per controllare lo stato della pipeline.  |
| [**D3D12_PIPELINE_STATE_SUBOBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type). Specifica il tipo di un oggetto secondario in una descrizione del flusso di stato della pipeline. |
| [**D3D12_PREDICATION_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_predication_op). Specifica l'operazione predicazione da applicare.  |
| [**D3D12_PRIMITIVE_TOPOLOGY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type). Specifica il modo in cui la pipeline interpreta le primitive di input di geometria o Hull shader. |
| [**D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_programmable_sample_positions_tier). Specifica il livello di supporto per le posizioni di esempio programmabili offerte dall'adapter. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_flags). Definisce le costanti che specificano i flag di sessione delle risorse protette. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_support_flags). Definisce le costanti che specificano il supporto della sessione di risorse protette. |
| [**D3D12_PROTECTED_SESSION_STATUS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_session_status). Definisce le costanti che specificano lo stato della sessione protetta. |
| [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type). Specifica il tipo di heap di query da creare. |
| [**D3D12_QUERY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Specifica il tipo di query. |
| [**D3D12_RAY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_ray_flags). Flag passati alla funzione [**TraceRay**](./traceray-function.md) per eseguire l'override della trasparenza, dell'eliminazione e del comportamento iniziale. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags). Specifica i flag per la compilazione di una struttura di accelerazione raytracing. Usare un valore di questa enumerazione con la struttura di [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) che fornisce l'input per l'operazione di compilazione della struttura di accelerazione. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode). Specifica il tipo di operazione di copia eseguita durante la chiamata a [**CopyRaytracingAccelerationStructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_type). Specifica il tipo di informazioni di post-compilazione della struttura di accelerazione che possono essere recuperate con le chiamate a [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) e [**BuildRaytracingAccelerationStructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_type). Specifica il tipo di una struttura di accelerazione raytracing. |
| [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags). Specifica i flag per la geometria Raytracing in una struttura [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc) . |
| [**D3D12_RAYTRACING_GEOMETRY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_type). Specifica il tipo di geometria utilizzato per Raytracing. Usare un valore di questa enumerazione per specificare il tipo di geometria in un [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). |
| [**D3D12_RAYTRACING_INSTANCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_instance_flags). Flag per un'istanza della struttura di accelerazione raytracing. Questi flag possono essere utilizzati per eseguire l'override [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags) per le singole istanze. |
| [**D3D12_RAYTRACING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_tier). Specifica il livello di supporto per la traccia dei raggi sul dispositivo di grafica. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type). Specifica il tipo di accesso assegnato a un'applicazione per la risorsa o le risorse specificate in fase di transizione in un passaggio di rendering. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type). Specifica il tipo di accesso assegnato a un'applicazione per la risorsa o le risorse specificate in fase di transizione da un passaggio di rendering. |
| [**D3D12_RENDER_PASS_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_flags). Specifica la natura del passaggio di rendering. ad esempio, se si tratta di un passaggio di rendering di sospensione o di ripresa. |
| [**D3D12_RESIDENCY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_flags). Usato con la funzione EnqueueMakeResident per scegliere il modo in cui le operazioni di residenza procedono quando viene superato il budget di memoria. |
| [**D3D12_RESIDENCY_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_priority). Specifica bucket di priorità di residenza ampi utili per stabilire rapidamente uno schema di priorità dell'applicazione. |
| [**D3D12_RESOLVE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resolve_mode). Specifica un'operazione di risoluzione. |
| [**D3D12_RESOURCE_BARRIER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags). Flag per l'impostazione delle barriere delle risorse divise.  |
| [**D3D12_RESOURCE_BARRIER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_type). Specifica un tipo di barriera della risorsa (transizione nella descrizione dell'utilizzo delle risorse). |
| [**D3D12_RESOURCE_BINDING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_binding_tier). Identifica il livello di associazione di risorse in uso.  |
| [**D3D12_RESOURCE_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension). Identifica il tipo di risorsa in uso. |
| [**D3D12_RESOURCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_flags). Specifica le opzioni per l'utilizzo delle risorse.  |
| [**D3D12_RESOURCE_HEAP_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_heap_tier). Specifica il livello dell'heap delle risorse supportato dall'hardware e dal driver.  |
| [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states). Specifica lo stato di una risorsa relativa alla modalità di utilizzo della risorsa.  |
| [**D3D12_ROOT_DESCRIPTOR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags). Specifica la volatilità dei dati a cui fanno riferimento i descrittori in una descrizione della firma radice 1,1, che può abilitare alcune ottimizzazioni del driver. |
| [**D3D12_ROOT_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_parameter_type). Specifica il tipo di slot della firma radice.  |
| [**D3D12_ROOT_SIGNATURE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags). Specifica le opzioni per il layout della firma radice.  |
| [**D3D12_RTV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_rtv_dimension). Identifica il tipo di risorsa da visualizzare come destinazione di rendering. |
| [**D3D12_SHADER_CACHE_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_support_flags). Viene descritto il livello di supporto per la memorizzazione nella cache dello shader nel driver grafico corrente. |
| [**D3D12_SHADER_COMPONENT_MAPPING**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_component_mapping). Specifica il modo in cui la memoria viene instradata da una visualizzazione risorse dello shader (SRV).  |
| [**D3D12_SHADER_MIN_PRECISION_SUPPORT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_min_precision_support). Descrive le opzioni di supporto della precisione minima per gli shader nel driver grafico corrente.  |
| [**D3D12_SHADER_VISIBILITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility). Specifica gli shader che possono accedere al contenuto di un dato slot della firma radice. |
| [**D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shared_resource_compatibility_tier). Definisce le costanti che specificano un livello di supporto per la condivisione tra API. |
| [**D3D12_SRV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_srv_dimension). Identifica il tipo di risorsa che verrà visualizzata come una risorsa shader. |
| [**D3D12_STATIC_BORDER_COLOR**](/windows/win32/api/d3d12/ne-d3d12-d3d12_static_border_color). Specifica il colore del bordo per un campionatore statico.  |
| [**D3D12_STENCIL_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_stencil_op). Identifica le operazioni dello stencil che possono essere eseguite durante i test di stencil di profondità. |
| [**D3D12_TEXTURE_ADDRESS_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_address_mode). Identifica una tecnica per la risoluzione di coordinate di trama esterne ai limiti di una trama.  |
| [**D3D12_TEXTURE_COPY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_copy_type). Specifica il tipo di copia di trama che deve essere eseguita. |
| [**D3D12_TEXTURE_LAYOUT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_layout). Specifica le opzioni di layout della trama.  |
| [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags). Specifica come copiare un riquadro.  |
| [**D3D12_TILE_MAPPING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_mapping_flags). Specifica come eseguire un'operazione di mapping dei riquadri.  |
| [**D3D12_TILE_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_range_flags). Specifica un intervallo di mapping dei riquadri.  |
| [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier). Identifica il livello di livello al quale sono supportate le risorse affiancate.  |
| [**D3D12_UAV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_uav_dimension). Identifica le opzioni di visualizzazione accessi non ordinate. |
| [**D3D12_VIEW_INSTANCING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_flags). Specifica le opzioni per le istanze della visualizzazione. |
| [**D3D12_VIEW_INSTANCING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_tier). Indica il livello di livello al quale sono supportate le istanze di visualizzazione. |
| [**D3D12_WRITEBUFFERIMMEDIATE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_writebufferimmediate_mode). Specifica la modalità usata da un'operazione **WriteBufferImmediate** . |

## <a name="related-topics"></a>Argomenti correlati

* [Riferimento principale](direct3d-12-core-reference.md)
* [Guida di riferimento a Direct3D 12](direct3d-12-reference.md)