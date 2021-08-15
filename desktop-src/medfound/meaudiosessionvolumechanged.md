---
description: Inviato dal renderer audio di streaming (SAR) quando cambia lo stato del volume o dell'audio della sessione audio.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: Evento MEAudioSessionVolumeChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721de9751cac284cb25d390d948f0f686447c04eaa613c1fecd4bf3503bce76d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465401"
---
# <a name="meaudiosessionvolumechanged-event"></a>EVENTO MEAudioSessionVolumeChanged

Inviato dal renderer audio di streaming (SAR) quando cambia lo stato del volume o dell'audio della sessione audio.

La sessione multimediale inoltra questo evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Nessun dato dell'evento.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Puntatore [**all'interfaccia IMFAudioPolicy.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene generato dal sink di flusso della SAR. L'evento viene attivato quando la SAR riceve un evento [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) dalla sessione audio. Per ottenere il nuovo livello di volume e lo stato di disattivazione, chiamare [**IMFSimpleAudioVolume::GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) e [**IMFSimpleAudioVolume::GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).

La SAR invia questo evento se un'azione esterna modifica il volume, ad esempio se l'utente modifica il volume tramite il programma di controllo del volume di sistema (SndVol). La SAR non invia l'evento se l'applicazione modifica il volume direttamente nella SAR.

Inoltre, la SAR non invia questo evento quando il volume del canale cambia ([**IAudioSessionEvents::OnChannelVolumeChanged).**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)

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

 

 
