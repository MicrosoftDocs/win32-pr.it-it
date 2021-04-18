---
description: Inviato dal renderer di streaming audio (SAR) quando cambia lo stato del volume o del silenziamento della sessione audio.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: Evento MEAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429edd8a26ed7f4ca1e764c7fbea1c6930c4871c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308272"
---
# <a name="meaudiosessionvolumechanged-event"></a>Evento MEAudioSessionVolumeChanged

Inviato dal renderer di streaming audio (SAR) quando cambia lo stato del volume o del silenziamento della sessione audio.

La sessione multimediale trasmette questo evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ vuoto<br/>   | Nessun dato dell'evento.<br/> <br/>                                                     |
| VT \_ sconosciuto<br/> | Puntatore all'interfaccia [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene generato dal sink di flusso del SAR. L'evento viene generato quando il SAR riceve un evento [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) dalla sessione audio. Per ottenere il nuovo livello di volume e lo stato di silenziamento, chiamare [**IMFSimpleAudioVolume:: GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) e [**IMFSimpleAudioVolume:: getmute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).

Il SAR Invia questo evento se un'azione esterna modifica il volume, ad esempio se l'utente modifica il volume tramite il programma di controllo del volume di sistema (SndVol). Il SAR non invia l'evento se l'applicazione modifica il volume direttamente sulla SAR.

Inoltre, il SAR non invia questo evento quando il volume del canale cambia ([**IAudioSessionEvents:: OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).

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

 

 
