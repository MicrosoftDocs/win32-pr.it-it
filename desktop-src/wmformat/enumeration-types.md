---
title: Tipi di enumerazione di Windows Media Format SDK
description: Informazioni sui tipi di enumerazione implementati da Windows Media Format SDK, ad esempio DRM_HTTP_STATUS e DRM_LICENSE_STATE_CATEGORY.
ms.assetid: cd28f608-25ba-44a7-868b-b1cd4dfcfa45
keywords:
- Windows Media Format SDK, tipi di enumerazione
- Advanced Systems Format (ASF), tipi di enumerazione
- ASF (Advanced Systems Format), tipi di enumerazione
- tipi di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a6fcb6d433079cce9d570a7eb6e28f31691985
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112067997"
---
# <a name="windows-media-format-sdk-enumeration-types"></a>Tipi di enumerazione di Windows Media Format SDK

Windows Media Format SDK implementa i tipi di enumerazione seguenti.



| Tipo di enumerazione                                                               | Descrizione                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**STATO \_ HTTP \_ DRM**](drm-http-status.md)                                   | Definisce un intervallo di stati per una richiesta DRM.                                                                                     |
| [**CATEGORIA STATO \_ LICENZA \_ \_ DRM**](drm-license-state-category.md)            | Definisce le categorie per le stringhe di licenza DRM.                                                                                  |
| [**STATO \_ DI INDIVIDUALIZZAZIONE \_ DRM**](drm-individualization-status.md)         | Definisce gli stati validi per l'individualizzazione DRM.                                                                              |
| [**IMPOSTAZIONI \_ URLCREDPOLICY \_ DI NETSOURCE**](/previous-versions/windows/desktop/api/wmsinternaladminnetsource/ne-wmsinternaladminnetsource-netsource_urlcredpolicy_settings) | Definisce le possibili impostazioni dei criteri di sicurezza che possono esistere in un computer client.                                                   |
| [**WM \_ AETYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wm_aetype)                                                | Specifica le autorizzazioni per una voce in un elenco di accesso agli indirizzi IP.                                                             |
| [**TIPO DI \_ DATI WMT ATTR \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype)                               | Definisce un intervallo di tipi di dati di base. Questi valori vengono usati per identificare il tipo di dati restituiti dai vari metodi in questo SDK. |
| [**TIPO DI \_ IMMAGINE WMT ATTR \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_imagetype)                             | Definisce un intervallo di tipi di immagine che possono essere archiviati in un'intestazione di file ASF.                                                         |
| [**TIPO DI INFORMAZIONI SUL CODEC WMT \_ \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_codec_info_type)                          | Definisce un intervallo di dimensioni dei dati usate da un codec.                                                                                   |
| [**FLAG DI CREDENZIALI WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_credential_flags)                         | Definisce i flag che possono essere usati durante l'acquisizione delle credenziali.                                                                   |
| [**ATTENDIBILITÀ \_ DRMLA WMT \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust)                                   | Definisce lo stato di attendibilità di un URL di acquisizione della licenza DRM.                                                                        |
| [**FILE WMT \_ MODALITÀ \_ DI VISUALIZZAZIONE**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_filesink_mode)                               | Definisce i tipi di input accettati dal sink di file.                                                                            |
| [**TIPO DI IMMAGINE WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_image_type)                                     | Definisce i tipi di immagine possibili usati per gli annunci banner.                                                                            |
| [**TIPO DI INDICE WMT \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_index_type)                                     | Definisce l'oggetto a cui è possibile associare un indice basato sul tempo.                                                              |
| [**TIPO \_ DI \_ INDICIZZATORE WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_indexer_type)                                 | Definisce i tipi di indicizzazione supportati dall'indicizzatore.                                                                          |
| [**PROTOCOLLO NET WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_net_protocol)                                 | Definisce i tipi di protocolli supportati dal sink di rete.                                                                   |
| [**MODALITÀ CLASSE \_ WMT MUSICSPEECH \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_musicspeech_class_mode)            | Definisce le modalità di compressione disponibili per il codec Windows Media Audio 9 Voice.                                                |
| [**FORMATO OFFSET \_ WMT \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_offset_format)                               | Definisce i tipi di offset usati in questo SDK.                                                                                   |
| [**MODALITÀ \_ DI RIPRODUZIONE WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_play_mode)                                       | Definisce le opzioni di riproduzione del lettore.                                                                                      |
| [**IMPOSTAZIONI PROXY WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_proxy_settings)                             | Definisce le impostazioni del proxy di rete da usare con un oggetto lettore.                                                                 |
| [**DIRITTI \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights)                                              | Definisce i diritti che possono essere specificati in una licenza DRM.                                                                       |
| [**STATO \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status)                                              | Definisce un intervallo di flag di stato.                                                                                                 |
| [**FORMATO DI ARCHIVIAZIONE WMT \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format)                             | Definisce i tipi di file che possono essere manipolati con questo SDK.                                                                    |
| [**SELEZIONE \_ FLUSSO WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection)                         | Definisce lo stato di un flusso.                                                                                                  |
| [**TIPO DI TRASPORTO WMT \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_transport_type)                             | Definisce i tipi di trasporto supportati da questo SDK.                                                                               |
| [**VERSIONE \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version)                                            | Definisce i numeri di versione di Windows Media Format SDK.                                                                     |
| [**TIPO DI VOCE FILIGRANA WMT \_ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_watermark_entry_type)                | Definisce i tipi di filigrane supportate.                                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 




