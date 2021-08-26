---
title: Windows Strutture di Media Format SDK
description: Windows Strutture di Media Format SDK
ms.assetid: 118ef278-ca4f-4c30-9633-a2d851f5c758
keywords:
- Windows Media Format SDK, strutture
- Advanced Systems Format (ASF), strutture
- ASF (Advanced Systems Format), strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 319be2d061132f59c1c75ebb295c8ceb8ae87ffbcce48e8259a1faedcf18d666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006611"
---
# <a name="windows-media-format-sdk-structures"></a>Windows Strutture di Media Format SDK

L Windows Media Format SDK implementa le strutture seguenti.



| Struttura                                                                                | Descrizione                                                                                                                                                               |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DRM \_ COPY \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl)                                                   | Contiene informazioni sul livello di protezione di output applicabili all'azione di copia in una licenza DRM.                                                                               |
| [**DATI SULLO STATO \_ DELLA \_ LICENZA \_ DRM**](drm-license-state-data.md)                              | Contiene [*informazioni sulla*](wmformat-glossary.md) licenza relative a un diritto [*DRM*](wmformat-glossary.md) specificato. |
| [**LIVELLI MINIMI \_ DI \_ PROTEZIONE \_ DELL'OUTPUT \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) | Contiene i livelli minimi di protezione dell'output richiesti da una licenza DRM per riprodurre il contenuto in vari formati.                                                                      |
| [**ID \_ DI OUTPUT OPL DRM \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_opl_output_ids)                                      | Contiene una matrice di identificatori di tecnologia DRM. Questa struttura viene usata per definire gruppi di tecnologie in altre strutture DRM.                                            |
| [**DRM \_ PLAY \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl)                                                   | Contiene informazioni sul livello di protezione dell'output applicabili all'azione di riproduzione in una licenza DRM.                                                                               |
| [**ID CONTENUTO PLAYLIST DRM \_ \_ \_**](drm-playlist-content-id.md)                            | Contiene informazioni sul contenuto che deve essere copiato su CD come parte di una masterizzazione della playlist.                                                                                 |
| [**DRM \_ VAL16**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-drm_val16)                                                          | Archivia un valore a 128 bit usato come identificatore di dispositivo.                                                                                                                       |
| [**PROTEZIONE \_ DELL'OUTPUT VIDEO \_ \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_output_protection)                    | Contiene l'identificatore di una tecnologia di protezione video e i dati di configurazione richiesti da tale tecnologia.                                                             |
| [**ID DI \_ PROTEZIONE \_ DELL'OUTPUT VIDEO \_ \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids)           | Contiene una matrice di **strutture DRM \_ VIDEO OUTPUT \_ \_ PROTECTION.**                                                                                                          |
| [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85))                                                | Definisce il formato dei dati waveform-audio.                                                                                                                                |
| [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))                                | Definisce il formato dei dati waveform-audio per i formati con più di due canali.                                                                                      |
| [**ACCESSO \_ \_ ALL'INDIRIZZO WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_address_accessentry)                               | Specifica una voce in un elenco di accesso agli indirizzi IP.                                                                                                                          |
| [**PROPRIETÀ \_ CLIENT \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties)                                   | Registra le informazioni sul client.                                                                                                                                     |
| [**PROPRIETÀ CLIENT WM \_ \_ \_ EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties_ex)                            | Registra le informazioni estese sul client.                                                                                                                            |
| [**WM \_ GET \_ LICENSE \_ DATA**](wm-get-license-data.md)                                    | Contiene informazioni su una licenza DRM.                                                                                                                                 |
| [**WM \_ INDIVIDUALIZE \_ STATUS**](wm-individualize-status.md)                             | Registra lo stato del processo [*di individualizzazione.*](wmformat-glossary.md)                                                                |
| [**COPPIA DI BUCKET WM \_ \_ \_ LEAKY**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair)                                  | Vengono descritti i requisiti di memorizzazione nel buffer per un file VBR (Variable-Bit-Rate).                                                                                                  |
| [**DATI \_ SULLO STATO DELLA \_ \_ LICENZA WM**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))                                | Incapsula una struttura [**DRM \_ LICENSE STATE \_ \_ DATA**](drm-license-state-data.md) che descrive i dati sullo stato della licenza DRM.                                              |
| [**TIPO \_ DI SUPPORTO \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)                                                 | Descrive un esempio di supporto.                                                                                                                                                 |
| [**WMMPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmmpeg2videoinfo)                                             | Descrive un flusso video MPEG-2.                                                                                                                                         |
| [**IMMAGINE \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)                                                        | Contiene i dati per [**l'attributo dei metadati complessi WM/Picture.**](wmpicture.md)                                                                                     |
| [**INTERVALLO \_ DI NUMERI DI PORTA \_ \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_port_number_range)                                  | Descrive l'intervallo di numeri di porta usati **dall'interfaccia IWMReaderNetworkConfig.**                                                                                     |
| [**CLIENTINFO \_ \_ LETTORE WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_clientinfo)                                   | Descrive il lettore client (lettore) che accede al flusso multimediale.                                                                                                          |
| [**STATISTICHE \_ \_ LETTORE WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics)                                   | Descrive le prestazioni di un'operazione di lettura.                                                                                                                         |
| [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat)                                                 | Definisce il formato di un flusso di script.                                                                                                                                    |
| [**\_RECORD DI PRIORITÀ DEL \_ \_ FLUSSO WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record)                        | Contiene un numero di flusso e specifica se il recapito di tale flusso è obbligatorio.                                                                                      |
| [**INFORMAZIONI \_ SUL TIPO DI FLUSSO \_ \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info)                                    | Contiene i dati per l'attributo di metadati complessi [**WM/StreamTypeInfo.**](wm-streamtypeinfo.md)                                                                      |
| [**TESTO DI WM \_ \_ SINCRONIZZATO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_synchronised_lyrics)                               | Contiene i dati per l'attributo di metadati complessi [**\_ sincronizzati WM/Lyrics.**](wm-lyrics-synchronised.md)                                                           |
| [**TESTO \_ UTENTE \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_text)                                                   | Contiene i dati per [**l'attributo dei metadati complessi WM/Text.**](wm-text.md)                                                                                          |
| [**\_URL \_ WEB UTENTE WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_web_url)                                            | Contiene i dati per l'attributo di metadati [**complessi WM/UserWebURL.**](wm-userweburl.md)                                                                              |
| [**STATISTICHE DI WM \_ \_ WRITER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics)                                   | Descrive le prestazioni di un'operazione di scrittura.                                                                                                                         |
| [**STATISTICHE DI WM \_ \_ WRITER \_ EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex)                            | Contiene statistiche estese del writer.                                                                                                                                      |
| [**CHIAVE CONTENUTO \_ DI IMPORTAZIONE \_ \_ WMDRM**](wmdrm-import-content-key.md)                          | Contiene la chiave contenuto usata nell'importazione di contenuto protetto.                                                                                                                |
| [**\_STRUCT INIT DI IMPORTAZIONE \_ \_ WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)                          | Contiene la chiave di sessione crittografata e la chiave contenuto usata nell'importazione di contenuto protetto.                                                                                      |
| [**CHIAVE DI SESSIONE \_ DI IMPORTAZIONE \_ \_ WMDRM**](wmdrm-import-session-key.md)                          | Contiene la chiave di sessione per l'importazione di contenuto protetto.                                                                                                                    |
| [**SEGMENTO DI BUFFER WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_buffer_segment)                                       | Contiene le informazioni necessarie per specificare un segmento in un pacchetto.                                                                                                      |
| [**DATI DELL'ESTENSIONE \_ WMT \_ \_ COLORSPACEINFO**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data)        | Contiene i dati per l'estensione dell'unità dati \_ WM SampleExtensionGUID \_ ColorSpaceInfo.                                                                                    |
| [**FILE \_ WMTINK \_ DATA \_ UNIT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_filesink_data_unit)                              | Contiene informazioni su un pacchetto.                                                                                                                                      |
| [**FRAMMENTO DI PAYLOAD WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_payload_fragment)                                   | Contiene le informazioni necessarie per estrarre un frammento di payload da un pacchetto.                                                                                           |
| [**DATI \_ DELL'ESTENSIONE TIMECODE WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)                    | Contiene un singolo time code SMPTE e le informazioni correlate.                                                                                                                |
| [**ESEMPIO \_ DI VIDEOIMAGE \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample)                                 | Contiene informazioni su un esempio di immagine video.                                                                                                                          |
| [**VOCE DEL LIMITE WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_watermark_entry)                                     | Contiene informazioni su un sistema di filigrana.                                                                                                                         |
| [**FORMATO \_ WEBSTREAM WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format)                                   | Contiene informazioni su un flusso Web.                                                                                                                                  |
| [**INTESTAZIONE DI ESEMPIO WEBSTREAM WMT \_ \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header)                    | Contiene informazioni sull'intestazione per gli esempi di flussi Web.                                                                                                                       |
| [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)                                           | Descrive le informazioni sulla bitmap e sul colore per un'immagine video.                                                                                                             |
| [**WMVIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader2)                                         | Descrive le informazioni sulla bitmap e sul colore per un'immagine video, tra cui [*interlacciato,*](wmformat-glossary.md)protezione della copia e proporzioni.       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 
