---
description: La tabella seguente descrive i principali tipi di supporti.
ms.assetid: 718a07f6-e2e4-4670-b9cf-982b53abffd2
title: Tipi principali (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5722cbad713f2fb9ae876e58941bde44c2e110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327328"
---
# <a name="major-types"></a>Tipi principali

La tabella seguente descrive i principali tipi di supporti.



| GUID                                                                                                                                                                                                                                  | Descrizione                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="MEDIATYPE_AnalogAudio"></span><span id="mediatype_analogaudio"></span><span id="MEDIATYPE_ANALOGAUDIO"></span><dl> <dt>**\_ANALOGAUDIO MEDIATYPE**</dt> </dl>         | Audio analogico.<br/>                                                                                  |
| <span id="MEDIATYPE_AnalogVideo"></span><span id="mediatype_analogvideo"></span><span id="MEDIATYPE_ANALOGVIDEO"></span><dl> <dt>**\_ANALOGVIDEO MEDIATYPE**</dt> </dl>         | Video analogo.<br/>                                                                                  |
| <span id="MEDIATYPE_Audio"></span><span id="mediatype_audio"></span><span id="MEDIATYPE_AUDIO"></span><dl> <dt>**\_Audio MEDIATYPE**</dt> </dl>                                 | Audio. Vedere [sottotipi audio](audio-subtypes.md).<br/>                                               |
| <span id="MEDIATYPE_AUXLine21Data"></span><span id="mediatype_auxline21data"></span><span id="MEDIATYPE_AUXLINE21DATA"></span><dl> <dt>**\_AUXLINE21DATA MEDIATYPE**</dt> </dl> | Dati della riga 21. Utilizzato da didascalie chiuse. Vedere la [**riga 21 tipi di supporto**](line-21-media-types.md).<br/> |
| <span id="MEDIATYPE_File"></span><span id="mediatype_file"></span><span id="MEDIATYPE_FILE"></span><dl> <dt>**\_File MEDIATYPE**</dt> </dl>                                     | File. (Obsoleto)<br/>                                                                               |
| <span id="MEDIATYPE_Interleaved"></span><span id="mediatype_interleaved"></span><span id="MEDIATYPE_INTERLEAVED"></span><dl> <dt>**MEDIATYPE con \_ interfoliazione**</dt> </dl>         | Audio e video con interfoliazione. Usato per video digitali (DV).<br/>                                      |
| <span id="MEDIATYPE_LMRT"></span><span id="mediatype_lmrt"></span><dl> <dt>**\_LMRT MEDIATYPE**</dt> </dl>                                                                      | Obsoleta. Non usare.<br/>                                                                          |
| <span id="MEDIATYPE_Midi"></span><span id="mediatype_midi"></span><span id="MEDIATYPE_MIDI"></span><dl> <dt>**MEDIATYPE \_ MIDI**</dt> </dl>                                     | Formato MIDI.<br/>                                                                                   |
| <span id="MEDIATYPE_MPEG2_PES"></span><span id="mediatype_mpeg2_pes"></span><dl> <dt>**\_PES MEDIATYPE MPEG2 \_**</dt> </dl>                                                      | Pacchetti MPEG-2 PES. Vedere [tipi di supporto MPEG-2](mpeg-2-media-types.md).<br/>                          |
| <span id="MEDIATYPE_MPEG2_SECTIONS"></span><span id="mediatype_mpeg2_sections"></span><dl> <dt>**\_Sezioni MEDIATYPE MPEG2 \_**</dt> </dl>                                       | Dati della sezione MPEG-2. Vedere [tipi di supporto MPEG-2](mpeg-2-media-types.md).<br/>                         |
| <span id="MEDIATYPE_ScriptCommand"></span><span id="mediatype_scriptcommand"></span><span id="MEDIATYPE_SCRIPTCOMMAND"></span><dl> <dt>**\_SCRIPTCOMMAND MEDIATYPE**</dt> </dl> | I dati sono un comando script, usato da didascalie chiuse.<br/>                                             |
| <span id="MEDIATYPE_Stream"></span><span id="mediatype_stream"></span><span id="MEDIATYPE_STREAM"></span><dl> <dt>**\_Flusso MEDIATYPE**</dt> </dl>                             | Flusso di byte senza timestamp. Vedere [**sottotipi di flusso**](stream-subtypes.md).<br/>               |
| <span id="MEDIATYPE_Text"></span><span id="mediatype_text"></span><span id="MEDIATYPE_TEXT"></span><dl> <dt>**\_Testo MEDIATYPE**</dt> </dl>                                     | Text.<br/>                                                                                          |
| <span id="MEDIATYPE_Timecode"></span><span id="mediatype_timecode"></span><span id="MEDIATYPE_TIMECODE"></span><dl> <dt>**MEDIATYPE \_ timecode**</dt> </dl>                     | Dati del timecode. Nota: DirectShow non fornisce filtri che supportano questo tipo di supporto.<br/>     |
| <span id="MEDIATYPE_URL_STREAM"></span><span id="mediatype_url_stream"></span><dl> <dt>**\_flusso URL \_ MEDIATYPE**</dt> </dl>                                                   | Obsoleta. Non usare.<br/>                                                                          |
| <span id="MEDIATYPE_VBI"></span><span id="mediatype_vbi"></span><dl> <dt>**\_VBI MEDIATYPE**</dt> </dl>                                                                         | Dati dell'intervallo di spazi vuoti verticali (VBI) (per la televisione). Uguale a KSDATAFORMAT di \_ tipo \_ VBI.<br/>       |
| <span id="MEDIATYPE_Video"></span><span id="mediatype_video"></span><span id="MEDIATYPE_VIDEO"></span><dl> <dt>**Video di MEDIATYPE \_**</dt> </dl>                                 | Video. Vedere [sottotipi video](video-subtypes.md).<br/>                                               |



## <a name="remarks"></a>Commenti

Il GUID del sottotipo definisce ulteriormente il formato. Per alcuni formati, il GUID del sottotipo potrebbe essere MEDIASUBTYPE \_ None, il che significa che il formato non richiede un sottotipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di supporto](media-types.md)
</dt> </dl>

 

 




