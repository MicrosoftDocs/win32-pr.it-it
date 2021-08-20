---
description: Nella tabella seguente vengono descritti i principali tipi di supporti.
ms.assetid: 718a07f6-e2e4-4670-b9cf-982b53abffd2
title: Tipi principali (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3764bffabb85b3b054fc7589d4eae9677adbc8835d0e4aa3029d31834eb887c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153243"
---
# <a name="major-types"></a>Tipi principali

Nella tabella seguente vengono descritti i principali tipi di supporti.



| GUID                                                                                                                                                                                                                                  | Descrizione                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="MEDIATYPE_AnalogAudio"></span><span id="mediatype_analogaudio"></span><span id="MEDIATYPE_ANALOGAUDIO"></span><dl> <dt>**MEDIATYPE \_ AnalogAudio**</dt> </dl>         | Audio analogico.<br/>                                                                                  |
| <span id="MEDIATYPE_AnalogVideo"></span><span id="mediatype_analogvideo"></span><span id="MEDIATYPE_ANALOGVIDEO"></span><dl> <dt>**MEDIATYPE \_ AnalogVideo**</dt> </dl>         | Video analogico.<br/>                                                                                  |
| <span id="MEDIATYPE_Audio"></span><span id="mediatype_audio"></span><span id="MEDIATYPE_AUDIO"></span><dl> <dt>**MEDIATYPE \_ Audio**</dt> </dl>                                 | Audio. Vedere [Sottotipi audio.](audio-subtypes.md)<br/>                                               |
| <span id="MEDIATYPE_AUXLine21Data"></span><span id="mediatype_auxline21data"></span><span id="MEDIATYPE_AUXLINE21DATA"></span><dl> <dt>**MEDIATYPE \_ AUXLine21Data**</dt> </dl> | Dati della riga 21. Utilizzato dai sottotitoli codificati. Vedere [**Line 21 Media Types ( Tipi di supporti per la riga 21).**](line-21-media-types.md)<br/> |
| <span id="MEDIATYPE_File"></span><span id="mediatype_file"></span><span id="MEDIATYPE_FILE"></span><dl> <dt>**MEDIATYPE \_ File**</dt> </dl>                                     | File. (Obsoleto)<br/>                                                                               |
| <span id="MEDIATYPE_Interleaved"></span><span id="mediatype_interleaved"></span><span id="MEDIATYPE_INTERLEAVED"></span><dl> <dt>**MEDIATYPE \_ Interleaved**</dt> </dl>         | Audio e video interleaved. Usato per video digitali (DV).<br/>                                      |
| <span id="MEDIATYPE_LMRT"></span><span id="mediatype_lmrt"></span><dl> <dt>**MEDIATYPE \_ LMRT**</dt> </dl>                                                                      | Obsoleta. Non usare.<br/>                                                                          |
| <span id="MEDIATYPE_Midi"></span><span id="mediatype_midi"></span><span id="MEDIATYPE_MIDI"></span><dl> <dt>**MEDIATYPE \_ Midi**</dt> </dl>                                     | Formato MIDI.<br/>                                                                                   |
| <span id="MEDIATYPE_MPEG2_PES"></span><span id="mediatype_mpeg2_pes"></span><dl> <dt>**MEDIATYPE \_ MPEG2 \_ PES**</dt> </dl>                                                      | Pacchetti PES MPEG-2. Vedere [MpEG-2 Media Types ( Tipi di supporti MPEG-2).](mpeg-2-media-types.md)<br/>                          |
| <span id="MEDIATYPE_MPEG2_SECTIONS"></span><span id="mediatype_mpeg2_sections"></span><dl> <dt>**SEZIONI \_ MPEG2 \_ MEDIATYPE**</dt> </dl>                                       | Dati della sezione MPEG-2. Vedere [MpEG-2 Media Types ( Tipi di supporti MPEG-2).](mpeg-2-media-types.md)<br/>                         |
| <span id="MEDIATYPE_ScriptCommand"></span><span id="mediatype_scriptcommand"></span><span id="MEDIATYPE_SCRIPTCOMMAND"></span><dl> <dt>**MEDIATYPE \_ ScriptCommand**</dt> </dl> | I dati sono un comando script, usato dai sottotitoli codificati.<br/>                                             |
| <span id="MEDIATYPE_Stream"></span><span id="mediatype_stream"></span><span id="MEDIATYPE_STREAM"></span><dl> <dt>**Flusso \_ MEDIATYPE**</dt> </dl>                             | Flusso di byte senza timestamp. Vedere [**Sottotipi di flusso**](stream-subtypes.md).<br/>               |
| <span id="MEDIATYPE_Text"></span><span id="mediatype_text"></span><span id="MEDIATYPE_TEXT"></span><dl> <dt>**Testo \_ MEDIATYPE**</dt> </dl>                                     | Text.<br/>                                                                                          |
| <span id="MEDIATYPE_Timecode"></span><span id="mediatype_timecode"></span><span id="MEDIATYPE_TIMECODE"></span><dl> <dt>**Codice \_ temporale MEDIATYPE**</dt> </dl>                     | Dati timecode. Nota: DirectShow non fornisce filtri che supportano questo tipo di supporto.<br/>     |
| <span id="MEDIATYPE_URL_STREAM"></span><span id="mediatype_url_stream"></span><dl> <dt>**FLUSSO URL MEDIATYPE \_ \_**</dt> </dl>                                                   | Obsoleta. Non usare.<br/>                                                                          |
| <span id="MEDIATYPE_VBI"></span><span id="mediatype_vbi"></span><dl> <dt>**MEDIATYPE \_ VBI**</dt> </dl>                                                                         | Dati dell'intervallo di blanking verticale (VBI) (per tv). Uguale a KSDATAFORMAT \_ TYPE \_ VBI.<br/>       |
| <span id="MEDIATYPE_Video"></span><span id="mediatype_video"></span><span id="MEDIATYPE_VIDEO"></span><dl> <dt>**MEDIATYPE \_ Video**</dt> </dl>                                 | Video. Vedere [Sottotipi video.](video-subtypes.md)<br/>                                               |



## <a name="remarks"></a>Commenti

Il GUID del sottotipo definisce ulteriormente il formato. Per alcuni formati, il GUID del sottotipo potrebbe essere MEDIASUBTYPE Nessuno, il che significa che il \_ formato non richiede un sottotipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di supporti](media-types.md)
</dt> </dl>

 

 




