---
description: Le costanti di tipo supporto sono definite di seguito.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: Costanti TAPIMEDIATYPE_ (Tapi3. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71a7d7ffb411d84e99863bb89274e43200b319d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331769"
---
# <a name="tapimediatype_-constants"></a>\_Costanti TAPIMEDIATYPE

Sono definiti i tipi di supporto seguenti:



| Costante/valore                                                                                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <dt>**TAPIMEDIATYPE \_**</dt> <dt>0x8</dt> audio </dl>                    | Un flusso multimediale audio che sta entrando o uscendo dal computer. Un flusso multimediale di immissione viene in genere riprodotto nei relatori o inviato a un dispositivo portatile e un flusso in uscita viene in genere acquisito tramite un dispositivo microfonico o ricevitore.<br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <dt>**TAPIMEDIATYPE \_ VIDEO**</dt> <dt>0x8000</dt> </dl>                 | Un flusso multimediale video che entra o esce dal computer. Viene in genere eseguito il rendering di un flusso multimediale di immissione in una finestra video e un flusso multimediale in uscita viene in genere acquisito con una videocamera video.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <dt>**TAPIMEDIATYPE \_ 0x10 DataModel**</dt> <dt></dt> </dl>       | Flusso multimediale dati associato a un modem dati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <dt>**TAPIMEDIATYPE \_**</dt> <dt>0x20</dt> G3FAX </dl>                   | Un flusso multimediale dati associato a un fax del protocollo G3.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <dt>**TAPIMEDIATYPE \_ 0x10000 multitraccia**</dt> <dt></dt> </dl> | Un flusso si trova in un terminale multitraccia.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <dt>**\_ \_ Flusso singolo RTP \_ MEDIATYPE**</dt> </dl>     | Questo GUID viene usato tra un terminale fornito dall'applicazione e il flusso del MSP. Se il pin del terminale supporta questo tipo di supporto, il flusso effettuerà lo scambio di dati RTP non elaborati con il terminale. Questa modalità è supportata solo dai flussi video in H323 MSP e IPConf MSP per Windows 2000 SP1 o versione successiva.<br/> **Intestazione:** Dichiarata in ipmsp. h. L'intestazione ipmsp. h non è disponibile in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                              |
| Intestazione<br/>       | <dl> <dt>Tapi3. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITQOSEvent:: Get \_ mediaType**](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[**ITAMMediaFormat:: Get \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[**ITAMMediaFormat::p UT \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[**ITMediaSupport:: Get \_ MediaTypes**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

