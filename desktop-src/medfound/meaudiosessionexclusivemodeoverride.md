---
description: Generato dal renderer audio quando la sessione audio viene superata da una connessione in modalità esclusiva. Il renderer audio non è ora valido.
ms.assetid: f89acfe4-14a7-4051-a816-e5e0ba8db80a
title: Evento MEAudioSessionExclusiveModeOverride (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3732be3fec73e3e948f6093187f32dd46839bea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226335"
---
# <a name="meaudiosessionexclusivemodeoverride-event"></a>Evento MEAudioSessionExclusiveModeOverride

Generato dal renderer audio quando la sessione audio viene superata da una connessione in modalità esclusiva. Il renderer audio non è ora valido.

La sessione multimediale trasmette questo evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ vuoto<br/>   | Nessun dato dell'evento.<br/> <br/>                                                     |
| VT \_ sconosciuto<br/> | Puntatore all'interfaccia [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene inviato dal sink di flusso del renderer audio. L'evento viene attivato quando il renderer audio riceve un evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) dalla sessione audio con il motivo di disconnessione uguale a DisconnectReasonExclusiveModeOverride.

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

 

 
