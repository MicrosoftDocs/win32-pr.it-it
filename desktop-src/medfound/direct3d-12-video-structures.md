---
description: Questa sezione contiene informazioni di riferimento per le strutture dell'API video Microsoft Direct3D 12.
ms.assetid: ''
title: Strutture video Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 945bb3f32a72cab437939e45a0b9691cbde70ef32acf7b08afd2580ff4a4259b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958751"
---
# <a name="direct3d-12-video-structures"></a>Strutture video Direct3D 12

Questa sezione contiene informazioni di riferimento per le strutture dell'API video Microsoft Direct3D 12.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento                                                                                | Descrizione                                                                                              |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support)  | Recupera l'elenco di profili supportati.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats)  | Recupera l'elenco dei formati supportati.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_histogram)  | Fornisce i dati per le chiamate a ID3D12VideoDevice::CheckFeatureSupport quando la funzionalità specificata è D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles)  | Recupera l'elenco di profili supportati.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_support)  | Recupera informazioni di supporto per la decodifica video.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_count)  | Recupera il numero di comandi di estensione video.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_parameter_count)  | Recupera il numero supportato di parametri per la fase del parametro specificata.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_parameters)  | Recupera l'elenco di parametri di comando dell'estensione video per la fase del parametro specificata.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_size)  | Controlla le dimensioni di allocazione di un comando di estensione video.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_support)  | Recupera il supporto dei comandi di estensione video usando strutture di input e output definite dal comando.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMANDS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_commands)  | Recupera l'elenco di comandi di estensione video dal driver.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator)  | Fornisce i dati per le chiamate a ID3D12VideoDevice::CheckFeatureSupport quando la funzionalità specificata è D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR. Recupera le funzionalità di stima del movimento per un codificatore video.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator_protected_resources)  | Fornisce i dati per le chiamate a ID3D12VideoDevice::CheckFeatureSupport quando la funzionalità specificata viene D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES. Recupera il supporto delle risorse protette per la stima del movimento video.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator_size)  | Descrive le dimensioni di allocazione di un heap dello stima del movimento video.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_max_input_streams)  | Recupera il numero massimo di flussi di input abilitati supportati dal processore video.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_reference_info)  | Recupera il numero di fotogrammi di riferimento passati e futuri necessari per le funzionalità di elaborazione automatica, filtro, conversione della frequenza o deinterlace specificate.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_support)  | Fornisce i dati per le chiamate a ID3D12VideoDevice::CheckFeatureSupport quando la funzionalità specificata viene D3D12_FEATURE_VIDEO_PROCESS_SUPPORT.|
| [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics)  | Rappresenta i dati per una query di statistiche di decodifica video richiamata chiamando ID3D12VideoDecodeCommandList::EndQuery.|
| [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resolve_video_motion_vector_heap_input)  | Fornisce dati di input per le chiamate a ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap.|
| [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resolve_video_motion_vector_heap_output)  | Riceve i dati di output dalle chiamate a ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap.|
| [D3D12_RESOURCE_COORDINATE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resource_coordinate)  | Descrive le coordinate di una risorsa.|
| [D3D12_VIDEO_DECODER_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_desc)  | Descrive un ID3D12VideoDecoder.|
| [D3D12_VIDEO_DECODER_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc)  | Descrive un ID3D12VideoDecoderHeap.|
| [D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_compressed_bitstream)  | Rappresenta un flusso di bit compresso da cui viene decodificato il video.|
| [D3D12_VIDEO_DECODE_CONFIGURATION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_configuration)  | Descrive la configurazione per un decodificatore video.|
| [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments)  | Specifica i parametri per la conversione dell'output di decodifica.|
| [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments1)  | Specifica i parametri per la conversione dell'output di decodifica.|
| [D3D12_VIDEO_DECODE_FRAME_ARGUMENT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_frame_argument)  | Rappresenta i parametri di decodifica per un frame.|
| [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)  | Specifica i parametri per il flusso di input per un'operazione di decodifica video.|
| [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram)  | Rappresenta il buffer di output dell'istogramma per un singolo componente.|
| [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments)  | Specifica i parametri per il flusso di output per un'operazione di decodifica video.|
| [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1)  | Specifica i parametri per il flusso di output per un'operazione di decodifica video.|
| [D3D12_VIDEO_DECODE_REFERENCE_FRAMES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_reference_frames)  | Contiene l'elenco dei fotogrammi di riferimento per l'operazione di decodifica corrente.|
| [D3D12_VIDEO_DECODE_SUB_SAMPLE_MAPPING_BLOCK](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_sub_sample_mapping_block)  | Definisce il mapping dei byte di crittografia degli esempi secondari per la decodifica video.|
| [D3D12_VIDEO_EXTENSION_COMMAND_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_desc)  | Descrive un comando di estensione video.|
| [D3D12_VIDEO_EXTENSION_COMMAND_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_info)  | Descrive un comando di estensione video.|
| [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_parameter_info)  | Descrive un parametro di comando dell'estensione video.|
| [D3D12_VIDEO_FORMAT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_format)  | Definisce la combinazione di formato pixel e spazio colore per una descrizione del contenuto della risorsa.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_desc)  | Descrive un ID3D12VideoMotionEstimator. Passare questa struttura in ID3D12VideoDevice1::CreateVideoMotionEstimator per creare un'istanza di ID3D12VideoMotionEstimator.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input)  | Fornisce dati di input per le chiamate a ID3D12VideoEncodeCommandList::EstimateMotion.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output)  | Riceve i dati di output dalle chiamate a ID3D12VideoEncodeCommandList::EstimateMotion.|
| [D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_vector_heap_desc)  | Descrive un ID3D12VideoMotionEstimatorHeap. Passare questa struttura in ID3D12VideoDevice1::CreateVideoMotionEstimatorHeap per creare un'istanza di ID3D12VideoMotionEstimatorHeap.|
| [D3D12_VIDEO_PROCESS_ALPHA_BLENDING](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_alpha_blending)  | Specifica i parametri di fusione alfa per l'elaborazione video.|
| [D3D12_VIDEO_PROCESS_FILTER_RANGE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_filter_range)  | Definisce l'intervallo di valori supportati per un filtro di immagine.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream)  | Contiene informazioni di input per la funzionalità di blend del processore video.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)  | Specifica gli argomenti del flusso di input per un flusso di input passato a ID3D12VideoCommandList::P rocessFrames.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc)  | Specifica i parametri per il flusso di input per un'operazione di processo video.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_RATE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_rate)  | Fornisce informazioni sulla frequenza del flusso.|
| [D3D12_VIDEO_PROCESS_LUMA_KEY](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_luma_key)  | Specifica le impostazioni usate per la chiave luma.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream)  | Rappresenta il flusso di output per i comandi di elaborazione video.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments)  | Specifica gli argomenti del flusso di output per l'output passato a ID3D12VideoCommandList::P rocessFrames.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  | Specifica gli argomenti del flusso di output per l'output passato a ID3D12VideoProcessCommandList::P rocessFrames.|
| [D3D12_VIDEO_PROCESS_REFERENCE_SET](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_reference_set)  | Contiene i fotogrammi di riferimento necessari per eseguire l'elaborazione video.|
| [D3D12_VIDEO_PROCESS_TRANSFORM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_transform)  | Specifica i parametri di trasformazione per l'elaborazione video.|
| [D3D12_VIDEO_SAMPLE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_sample)  | Descrive la larghezza, l'altezza, il formato e lo spazio colore di un buffer immagine.|
| [D3D12_VIDEO_SCALE_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_scale_support)  | Descrive l'intervallo di scalabilità supportato di dimensioni di output per un ridimensionatore video.|
| [D3D12_VIDEO_SIZE_RANGE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_size_range)  | Descrive l'intervallo di dimensioni supportate per un ridimensionatore video.|



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API video Direct3D 12](direct3d-12-video-apis.md)
</dt> </dl>

 

 



