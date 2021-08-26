---
description: Generato dal renderer audio quando cambia il formato audio predefinito per il dispositivo audio. Il renderer audio non è più valido.
ms.assetid: eeef764a-f6d2-4f6e-9af3-acd5fd7bc55c
title: Evento MEAudioSessionFormatChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab0464aa4bd98ec0143838762ac3fcc3efd88e03528b1d5732e2d5423a711640
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013871"
---
# <a name="meaudiosessionformatchanged-event"></a>Evento MEAudioSessionFormatChanged

Generato dal renderer audio quando cambia il formato audio predefinito per il dispositivo audio. Il renderer audio non è più valido.

La sessione multimediale inoltra questo evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Nessun dato dell'evento.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Puntatore [**all'interfaccia IMFAudioPolicy.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene inviato dal sink di flusso del renderer audio. L'evento viene attivato quando il renderer audio riceve un evento [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) dalla sessione audio in modalità utente con il motivo di disconnessione uguale a **DisconnectReasonFormatChanged.**

Il [**puntatore IMFAudioPolicy,**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) se impostato, non è utile perché il flusso audio non è più valido.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> <dt>

[Streaming Audio Renderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
