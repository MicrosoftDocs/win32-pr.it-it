---
title: Strutture di Windows Media Format SDK
description: Strutture di Windows Media Format SDK
ms.assetid: 118ef278-ca4f-4c30-9633-a2d851f5c758
keywords:
- Windows Media Format SDK, strutture
- ASF (Advanced Systems Format), strutture
- ASF (formato avanzato dei sistemi), strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f730ba3cbc5bd8bbec2a9f01c72df1fe46f0b64
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300892"
---
# <a name="windows-media-format-sdk-structures"></a>Strutture di Windows Media Format SDK

Windows Media Format SDK implementa le seguenti strutture.



| Struttura                                                                                | Descrizione                                                                                                                                                               |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_copia DRM \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl)                                                   | Include informazioni sul livello di protezione dell'output valide per l'azione di copia in una licenza DRM.                                                                               |
| [**\_ \_ dati sullo stato della licenza DRM \_**](drm-license-state-data.md)                              | Contiene informazioni sulla [*licenza*](wmformat-glossary.md) per un diritto [*DRM*](wmformat-glossary.md) specificato. |
| [**\_livelli di \_ protezione dell'output minimo \_ DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) | Include i livelli minimi di protezione dell'output richiesti da una licenza DRM per riprodurre contenuti in vari formati.                                                                      |
| [**\_ \_ ID output OPL \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_opl_output_ids)                                      | Include una matrice di identificatori di tecnologia DRM. Questa struttura viene utilizzata per definire gruppi di tecnologie in altre strutture DRM.                                            |
| [**\_riproduzione DRM \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl)                                                   | Include informazioni sul livello di protezione dell'output valide per l'azione di riproduzione in una licenza DRM.                                                                               |
| [**\_ \_ ID contenuto della playlist DRM \_**](drm-playlist-content-id.md)                            | Contiene informazioni sul contenuto che deve essere copiato su CD come parte di un'ustione della playlist.                                                                                 |
| [**\_VAL16 DRM**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-drm_val16)                                                          | Archivia un valore a 128 bit usato come identificatore del dispositivo.                                                                                                                       |
| [**\_protezione dell' \_ output del video DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_output_protection)                    | Include l'identificatore di una tecnologia di protezione video e i dati di configurazione richiesti da tale tecnologia.                                                             |
| [**\_ID di \_ protezione dell'output del video DRM \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids)           | Include una matrice di strutture di **\_ \_ \_ protezione dell'output video DRM** .                                                                                                          |
| [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85))                                                | Definisce il formato dei dati audio della forma d'onda.                                                                                                                                |
| [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))                                | Definisce il formato dei dati audio della forma d'onda per i formati che dispongono di più di due canali.                                                                                      |
| [**\_ACCESSENTRY indirizzo \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_address_accessentry)                               | Specifica una voce in un elenco di accesso di indirizzi IP.                                                                                                                          |
| [**\_proprietà client \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties)                                   | Registra le informazioni sul client.                                                                                                                                     |
| [**\_proprietà client \_ WM \_ ex**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties_ex)                            | Registra informazioni estese sul client.                                                                                                                            |
| [**WM \_ ottenere \_ \_ i dati di licenza**](wm-get-license-data.md)                                    | Contiene informazioni su una licenza DRM.                                                                                                                                 |
| [**\_stato di personalizzazione WM \_**](wm-individualize-status.md)                             | Registra lo stato del processo di [*individualizzazione*](wmformat-glossary.md) .                                                                |
| [**coppia di bucket a \_ perdita WM \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair)                                  | Descrive i requisiti di buffering per un file con velocità in bit variabile (VBR).                                                                                                  |
| [**\_ \_ dati dello stato di licenza WM \_**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))                                | Incapsula una struttura [**\_ \_ \_ dei dati di stato della licenza DRM**](drm-license-state-data.md) che descrive i dati sullo stato delle licenze DRM.                                              |
| [**\_tipo di supporto WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)                                                 | Descrive un esempio di supporto.                                                                                                                                                 |
| [**WMMPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmmpeg2videoinfo)                                             | Descrive un flusso video MPEG-2.                                                                                                                                         |
| [**immagine di WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)                                                        | Contiene i dati per l'attributo di metadati complessi [**WM/Picture**](wmpicture.md) .                                                                                     |
| [**\_intervallo di \_ numeri di porta WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_port_number_range)                                  | Descrive l'intervallo di numeri di porta usati dall'interfaccia **IWMReaderNetworkConfig** .                                                                                     |
| [**\_CLIENTINFO WM Reader \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_clientinfo)                                   | Descrive il lettore client (lettore) che accede al flusso multimediale.                                                                                                          |
| [**Statistiche di WM \_ Reader \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics)                                   | Descrive le prestazioni di un'operazione di lettura.                                                                                                                         |
| [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat)                                                 | Definisce il formato di un flusso di script.                                                                                                                                    |
| [**\_record di \_ priorità del flusso WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record)                        | Contiene un numero di flusso e specifica se il recapito di tale flusso è obbligatorio.                                                                                      |
| [**\_informazioni sul \_ tipo di flusso WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info)                                    | Contiene i dati per l'attributo di metadati complessi [**WM/StreamTypeInfo**](wm-streamtypeinfo.md) .                                                                      |
| [**\_Testi con sincronizzazione \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_synchronised_lyrics)                               | Contiene i dati per l'attributo di metadati complessi [**\_ sincronizzati WM/lyrics**](wm-lyrics-synchronised.md) .                                                           |
| [**\_testo utente \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_text)                                                   | Contiene i dati per l'attributo di metadati complessi [**WM/text**](wm-text.md) .                                                                                          |
| [**\_ \_ URL Web utente \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_web_url)                                            | Contiene i dati per l'attributo di metadati complessi [**WM/UserWebURL**](wm-userweburl.md) .                                                                              |
| [**\_statistiche del writer WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics)                                   | Descrive le prestazioni di un'operazione di scrittura.                                                                                                                         |
| [**Statistiche di WM \_ writer \_ \_ ex**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex)                            | Contiene le statistiche del writer estese.                                                                                                                                      |
| [**WMDRM \_ Importa \_ \_ chiave simmetrica**](wmdrm-import-content-key.md)                          | Include la chiave simmetrica utilizzata per l'importazione di contenuto protetto.                                                                                                                |
| [**\_struct WMDRM Import \_ init \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)                          | Include la chiave della sessione crittografata e la chiave simmetrica utilizzata per l'importazione di contenuto protetto.                                                                                      |
| [**WMDRM \_ importare \_ la \_ chiave della sessione**](wmdrm-import-session-key.md)                          | Include la chiave della sessione per l'importazione del contenuto protetto.                                                                                                                    |
| [**\_segmento buffer \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_buffer_segment)                                       | Contiene le informazioni necessarie per specificare un segmento in un pacchetto.                                                                                                      |
| [**\_dati dell' \_ estensione \_ COLORSPACEINFO di WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data)        | Contiene i dati per l' \_ estensione dell' \_ unità dati SampleExtensionGUID COLORSPACEINFO di WM.                                                                                    |
| [**\_unità dati WMT FILEsink \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_filesink_data_unit)                              | Contiene informazioni su un pacchetto.                                                                                                                                      |
| [**\_ \_ frammento payload WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_payload_fragment)                                   | Contiene le informazioni necessarie per estrarre un frammento di payload da un pacchetto.                                                                                           |
| [**\_dati dell' \_ estensione del timecode WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)                    | Contiene un solo codice di ora SMPTE e informazioni correlate.                                                                                                                |
| [**\_esempio WMT VIDEOIMAGE \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample)                                 | Contiene informazioni su un esempio di immagine video.                                                                                                                          |
| [**\_voce filigrana WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_watermark_entry)                                     | Contiene informazioni su un sistema di filigrana.                                                                                                                         |
| [**\_formato WEBSTREAM \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format)                                   | Contiene informazioni su un flusso Web.                                                                                                                                  |
| [**WMT \_ intestazione di \_ esempio webstream \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header)                    | Contiene informazioni di intestazione per gli esempi di flusso Web.                                                                                                                       |
| [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)                                           | Descrive le informazioni sulla bitmap e sui colori per un'immagine video.                                                                                                             |
| [**WMVIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader2)                                         | Descrive le informazioni sulla bitmap e sui colori per un'immagine video, incluse le proporzioni [*interlacciate*](wmformat-glossary.md), di protezione da copia e di proporzioni.       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 
