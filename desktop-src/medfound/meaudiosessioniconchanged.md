---
description: Generato dal renderer audio quando l'icona della sessione audio cambia.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Evento MEAudioSessionIconChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ce466cf88b93c9cf806a2a6b70f76b084e8aa0b2c8fb2910a7391337a13b2f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062460"
---
# <a name="meaudiosessioniconchanged-event"></a>EVENTO MEAudioSessionIconChanged

Generato dal renderer audio quando l'icona della sessione audio cambia.

La sessione multimediale inoltra questo evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Nessun dato dell'evento.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Puntatore [**all'interfaccia IMFAudioPolicy.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene inviato dal sink di flusso del renderer audio. L'evento viene attivato quando il renderer audio riceve un evento [**IAudioSessionEvents::OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) dalla sessione audio.

Per ottenere la nuova icona, chiamare [**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> <dt>

[Streaming Audio Renderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
