---
title: Windows Tipi di enumerazione di Media Format SDK
description: Informazioni sui tipi di enumerazione implementati da Windows Media Format SDK, ad esempio DRM_HTTP_STATUS e DRM_LICENSE_STATE_CATEGORY.
ms.assetid: cd28f608-25ba-44a7-868b-b1cd4dfcfa45
keywords:
- Windows MEDIA Format SDK, tipi di enumerazione
- Advanced Systems Format (ASF), tipi di enumerazione
- ASF (Advanced Systems Format),tipi di enumerazione
- tipi di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b3a53688e21e58b0d9509cc901a72399f26b9d758cac89511e66a76d740db1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848160"
---
# <a name="windows-media-format-sdk-enumeration-types"></a>Windows Tipi di enumerazione di Media Format SDK

L Windows Media Format SDK implementa i tipi di enumerazione seguenti.



| Tipo di enumerazione                                                               | Descrizione                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**STATO \_ HTTP \_ DRM**](drm-http-status.md)                                   | Definisce un intervallo di stati per una richiesta DRM.                                                                                     |
| [**CATEGORIA STATO \_ LICENZA \_ \_ DRM**](drm-license-state-category.md)            | Definisce le categorie per le stringhe di licenza DRM.                                                                                  |
| [**STATO \_ DI INDIVIDUALIZZAZIONE \_ DRM**](drm-individualization-status.md)         | Definisce gli stati validi per l'individualizzazione DRM.                                                                              |
| [**NETSOURCE \_ URLCREDPOLICY \_ SETTINGS**](/previous-versions/windows/desktop/api/wmsinternaladminnetsource/ne-wmsinternaladminnetsource-netsource_urlcredpolicy_settings) | Definisce le possibili impostazioni dei criteri di sicurezza che possono esistere in un computer client.                                                   |
| [**WM \_ AETYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wm_aetype)                                                | Specifica le autorizzazioni per una voce in un elenco di accesso agli indirizzi IP.                                                             |
| [**TIPO DI DATI ATTR WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype)                               | Definisce un intervallo di tipi di dati di base. Questi valori vengono usati per identificare il tipo di dati restituiti dai vari metodi in questo SDK. |
| [**WMT \_ ATTR \_ IMAGETYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_imagetype)                             | Definisce un intervallo di tipi di immagine che possono essere archiviati in un'intestazione di file ASF.                                                         |
| [**TIPO DI INFORMAZIONI \_ SUL \_ CODEC \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_codec_info_type)                          | Definisce un intervallo di dimensioni dei dati usato da un codec.                                                                                   |
| [**FLAG DELLE CREDENZIALI WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_credential_flags)                         | Definisce i flag che possono essere utilizzati durante l'acquisizione delle credenziali.                                                                   |
| [**ATTENDIBILITÀ \_ DRMLA WMT \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust)                                   | Definisce lo stato di attendibilità di un URL di acquisizione della licenza DRM.                                                                        |
| [**FILE WMT \_ MODALITÀ INK \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_filesink_mode)                               | Definisce i tipi di input accettati dal sink di file.                                                                            |
| [**TIPO DI \_ IMMAGINE \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_image_type)                                     | Definisce i tipi di immagine possibili usati per gli annunci banner.                                                                            |
| [**TIPO DI INDICE \_ \_ WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_index_type)                                     | Definisce l'oggetto a cui è possibile associare un indice basato sul tempo.                                                              |
| [**TIPO DI \_ INDICIZZATORE \_ WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_indexer_type)                                 | Definisce i tipi di indicizzazione supportati dall'indicizzatore.                                                                          |
| [**PROTOCOLLO NET WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_net_protocol)                                 | Definisce i tipi di protocolli supportati dal sink di rete.                                                                   |
| [**MODALITÀ CLASSE \_ WMT MUSICSPEECH \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_musicspeech_class_mode)            | Definisce le modalità di compressione disponibili per il codec Windows Media Audio 9 Voice.                                                |
| [**FORMATO OFFSET \_ \_ WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_offset_format)                               | Definisce i tipi di offset usati in questo SDK.                                                                                   |
| [**MODALITÀ DI RIPRODUZIONE WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_play_mode)                                       | Definisce le opzioni di riproduzione del lettore.                                                                                      |
| [**IMPOSTAZIONI PROXY WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_proxy_settings)                             | Definisce le impostazioni proxy di rete da utilizzare con un oggetto lettore.                                                                 |
| [**DIRITTI \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights)                                              | Definisce i diritti che possono essere specificati in una licenza DRM.                                                                       |
| [**STATO \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status)                                              | Definisce un intervallo di flag di stato.                                                                                                 |
| [**FORMATO DI ARCHIVIAZIONE \_ \_ WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format)                             | Definisce i tipi di file che possono essere manipolati con questo SDK.                                                                    |
| [**SELEZIONE DEL FLUSSO WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection)                         | Definisce lo stato di un flusso.                                                                                                  |
| [**TIPO DI \_ TRASPORTO \_ WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_transport_type)                             | Definisce i tipi di trasporto supportati da questo SDK.                                                                               |
| [**VERSIONE \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version)                                            | Definisce i numeri di versione di Windows Media Format SDK.                                                                     |
| [**TIPO DI VOCE FILIGRANA WMT \_ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_watermark_entry_type)                | Definisce i tipi di filigrane supportate.                                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 




