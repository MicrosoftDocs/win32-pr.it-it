---
description: Le costanti del tipo di supporto sono definite di seguito.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: TAPIMEDIATYPE_ costanti (Tapi3.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a702f5a061629f3fd8daa5ad742c65af12c43bbd92eec6896b143e4bd6a403c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866881"
---
# <a name="tapimediatype_-constants"></a>Costanti TAPIMEDIATYPE \_

Sono definiti i tipi di supporti seguenti:



| Costante/valore                                                                                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <dt>**TAPIMEDIATYPE \_ Audio**</dt> <dt>0x8</dt> </dl>                    | Flusso multimediale audio che entra o esce dal computer. Un flusso multimediale in ingresso viene in genere riprodotto sugli altoparlanti o inviato a un dispositivo portatile e un flusso in uscita viene in genere acquisito tramite un microfono o un dispositivo portatile.<br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <dt>**TAPIMEDIATYPE \_ Video**</dt> <dt>0x8000</dt> </dl>                 | Flusso multimediale video che entra o esce dal computer. Il rendering di un flusso multimediale in ingresso viene in genere eseguito in una finestra video e un flusso multimediale in uscita viene in genere acquisito con una videocamera.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <dt>**TAPIMEDIATYPE \_ DataMODEM**</dt> <dt>0x10</dt> </dl>       | Flusso multimediale dati associato a un modem dati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <dt>**TAPIMEDIATYPE \_ G3FAX**</dt> <dt>0x20</dt> </dl>                   | Flusso multimediale dati associato a un fax del protocollo G3.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <dt>**TAPIMEDIATYPE \_ MultiTRACK**</dt> <dt>0x10000</dt> </dl> | Un flusso si trova in un terminale multitraccia.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <dt>**Flusso singolo \_ MEDIATYPE \_ \_ RTP**</dt> </dl>     | Questo GUID viene usato tra un terminale fornito dall'applicazione e il flusso del msp. Se il pin del terminale supporta questo tipo di supporto, il flusso scambierà dati RTP non elaborati con il terminale. Questa modalità è supportata solo dai flussi video in H323 MSP e IPConf MSP per Windows 2000 SP1 o versioni successive.<br/> **Intestazione:** Dichiarato in ipmsp.h. L'intestazione ipmsp.h non è disponibile in in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                              |
| Intestazione<br/>       | <dl> <dt>Tapi3.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITQOSEvent::get \_ MediaType**](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[**ITAMMediaFormat::get \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[**ITAMMediaFormat::put \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[**ITMediaSupport::get \_ MediaTypes**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

