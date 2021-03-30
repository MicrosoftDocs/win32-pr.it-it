---
title: Enumerazioni di livelli
description: Questa sezione contiene informazioni sulle enumerazioni dei livelli.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- enumerazioni, livello Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e1cca3fa500a529930c8d0c39005697045d18b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104976919"
---
# <a name="layer-enumerations"></a>Enumerazioni di livelli

Questa sezione contiene informazioni sulle enumerazioni dei livelli.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Categoria del messaggio d3d11 \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | Categorie di messaggi di debug. Questa operazione identificherà la categoria di un messaggio quando si recupera un messaggio con [**ID3D11InfoQueue:: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) e quando si aggiunge un messaggio con [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). Quando si crea un [**filtro coda informazioni**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), questi valori possono essere usati per consentire o negare a qualsiasi categoria di messaggi di passare attraverso i filtri di archiviazione e recupero.<br/> |
| [**\_ID messaggio \_ d3d11**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | Messaggi di debug per la configurazione di un filtro di Accodamento informazioni (vedere [**d3d11 \_ info \_ Queue \_ Filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); usare questi messaggi per consentire o negare alle categorie di messaggi di passare attraverso i filtri di archiviazione e recupero. Questi ID vengono usati da metodi quali [**ID3D11InfoQueue:: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) o [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). <br/>                                                             |
| [**\_Gravità del messaggio d3d11 \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | Livelli di gravità dei messaggi di debug per una coda di informazioni.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_Flag RLDO \_ d3d11**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | Opzioni per la quantità di informazioni per segnalare la durata di un oggetto dispositivo.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**\_ \_ Opzioni di rilevamento Shader \_ d3d11**](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | Opzioni che specificano come eseguire il rilevamento del debug dello shader.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**\_Tipo di risorsa di rilevamento Shader d3d11 \_ \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | Indica i tipi di risorse da rilevare.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al livello](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





