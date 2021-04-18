---
title: Enumerazioni del livello di debug
description: Le enumerazioni seguenti sono dichiarate in d3d12sdklayers. h.
ms.assetid: 6E76C857-128E-4F0E-9711-72C4CF6C835C
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746c0def35c8eb282264cb4ab0b40eb5c08f0f9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298677"
---
# <a name="debug-layer-enumerations"></a>Enumerazioni del livello di debug

Le enumerazioni seguenti sono dichiarate in d3d12sdklayers. h.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Tipo di \_ parametro dell'elenco di comandi di debug D3D12 \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)<br/>                                 | Indica il tipo di parametro di debug utilizzato da [**ID3D12DebugCommandList1:: SetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-setdebugparameter) e [**ID3D12DebugCommandList1:: GetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-getdebugparameter).<br/>                                                                                                                                                                                                      |
| [**\_Tipo di \_ parametro del dispositivo di debug D3D12 \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)<br/>                                              | Specifica il tipo di dati della memoria a cui punta il parametro *pData* di [**ID3D12DebugDevice1:: SetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) e [**ID3D12DebugDevice1:: GetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-getdebugparameter).<br/>                                                                                                                                                                                        |
| [**\_Funzionalità di debug D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature)<br/>                                                                            | Flag per le funzionalità facoltative del livello di debug di D3D12.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**\_Flag di \_ convalida basati sulla GPU \_ D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_flags)<br/>                                                | Descrive il livello di convalida basata su GPU da eseguire in fase di esecuzione.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**D3D12 \_ \_ \_ \_ \_ \_ creare flag per lo stato della pipeline di convalida basata \_ sulla GPU**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)<br/> | Specifica il modo in cui GPU-Based convalida gestisce gli Stati della pipeline con patch durante [**ID3D12Device:: CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) e [**ID3D12Device:: CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate).<br/>                                                                                                                                                                             |
| [**\_ \_ \_ \_ \_ Modalità patch shader di convalida basata su \_ GPU D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)<br/>                      | Specifica il tipo di applicazione di patch dello shader usato dalla convalida GPU-Based a livello di dispositivo o elenco di comandi.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**\_Categoria del messaggio D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_category)<br/>                                                                      | Specifica le categorie di messaggi di debug. Questa operazione identificherà la categoria di un messaggio quando si recupera un messaggio con [**ID3D12InfoQueue:: GetMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) e quando si aggiunge un messaggio con [**ID3D12InfoQueue:: AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage). Quando si crea un filtro coda informazioni, questi valori possono essere usati per consentire o negare a qualsiasi categoria di messaggi di passare attraverso i filtri di archiviazione e recupero. <br/> |
| [**\_ID messaggio \_ D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_id)<br/>                                                                                  | Specifica gli ID dei messaggi di debug per la configurazione di un filtro per la coda delle informazioni (vedere [**D3D12 \_ info \_ Queue \_ Filter**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)); usare questi messaggi per consentire o negare alle categorie di messaggi di passare attraverso i filtri di archiviazione e recupero. Questi ID vengono usati da metodi quali [**ID3D12InfoQueue:: GetMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) o [**ID3D12InfoQueue:: AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage). <br/>                        |
| [**\_Gravità del messaggio D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity)<br/>                                                                      | Livelli di gravità dei messaggi di debug per una coda di informazioni.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_Flag RLDO \_ D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_rldo_flags)<br/>                                                                                  | Specifica le opzioni per la quantità di informazioni da segnalare sulla durata di un oggetto dispositivo attivo. <br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dell'ambiente di programmazione Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Riferimento al livello di debug](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Guida di riferimento a Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





