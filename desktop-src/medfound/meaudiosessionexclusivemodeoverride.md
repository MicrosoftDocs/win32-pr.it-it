---
description: Generato dal renderer audio quando la sessione audio viene preempted da una connessione in modalità esclusiva. Il renderer audio non è più valido.
ms.assetid: f89acfe4-14a7-4051-a816-e5e0ba8db80a
title: Evento MEAudioSessionExclusiveModeOverride (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6344a5d073e9dc29777e6cb181c77bcae79da8602b830ade86646459e4d0bea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114221"
---
# <a name="meaudiosessionexclusivemodeoverride-event"></a>EVENTO MEAudioSessionExclusiveModeOverride

Generato dal renderer audio quando la sessione audio viene preempted da una connessione in modalità esclusiva. Il renderer audio non è più valido.

La sessione multimediale inoltra questo evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Nessun dato dell'evento.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Puntatore [**all'interfaccia IMFAudioPolicy.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene inviato dal sink di flusso del renderer audio. L'evento viene attivato quando il renderer audio riceve un evento [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) dalla sessione audio con il motivo di disconnessione uguale a DisconnectReasonExclusiveModeOverride.

Il [**puntatore IMFAudioPolicy,**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) se impostato, non è utile perché il flusso audio non è più valido.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> <dt>

[Streaming Audio Renderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
