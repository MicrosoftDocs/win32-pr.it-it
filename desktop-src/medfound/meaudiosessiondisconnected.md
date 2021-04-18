---
description: Generato dal renderer audio quando la sessione audio è disconnessa da una sessione di Servizi terminal di Windows (WTS). Il renderer audio non è ora valido.
ms.assetid: 08f9844c-f3b1-4d60-990e-9131f3312f6b
title: Evento MEAudioSessionDisconnected (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db2d31349585d26c61cb2940cea70ddaf0617901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308276"
---
# <a name="meaudiosessiondisconnected-event"></a>Evento MEAudioSessionDisconnected

Generato dal renderer audio quando la sessione audio è disconnessa da una sessione di Servizi terminal di Windows (WTS). Il renderer audio non è ora valido.

La sessione multimediale trasmette questo evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ vuoto<br/>   | Nessun dato dell'evento.<br/> <br/>                                                     |
| VT \_ sconosciuto<br/> | Puntatore all'interfaccia [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene inviato dal sink di flusso del renderer audio. L'evento viene attivato quando il renderer audio riceve un evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) dalla sessione audio con il motivo di disconnessione uguale a DisconnectReasonSessionDisconnected.

Il puntatore [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , se impostato, non è utile perché il flusso audio non è più valido.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> <dt>

[Renderer audio di streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
