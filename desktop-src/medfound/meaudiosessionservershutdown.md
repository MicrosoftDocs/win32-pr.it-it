---
description: Generato dal renderer audio quando il sistema server audio Windows viene arrestato. Il renderer audio non è ora valido.
ms.assetid: 8e80903c-d6ce-4fa2-87db-552c7fba3c6a
title: Evento MEAudioSessionServerShutdown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d819d850df481477b2ea1a5052c18d140a41cdb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308273"
---
# <a name="meaudiosessionservershutdown-event"></a>Evento MEAudioSessionServerShutdown

Generato dal renderer audio quando il sistema server audio Windows viene arrestato. Il renderer audio non è ora valido.

La sessione multimediale trasmette questo evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ vuoto<br/>   | Nessun dato dell'evento.<br/> <br/>                                                     |
| VT \_ sconosciuto<br/> | Puntatore all'interfaccia [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene inviato dal sink di flusso del renderer audio. L'evento viene attivato quando il renderer audio riceve un evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) dalla sessione audio con il motivo di disconnessione uguale a **DisconnectReasonServerShutdown**.

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

 

 
