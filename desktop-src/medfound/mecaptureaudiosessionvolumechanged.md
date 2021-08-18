---
description: Inviato da un'origine di acquisizione audio quando il volume cambia.
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: Evento MECaptureAudioSessionVolumeChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f2e83bdf03f61abac733a5e06310ff12c0797664d6a2405aed97210bf5ff42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878083"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a>Evento MECaptureAudioSessionVolumeChanged

Inviato da un'origine di acquisizione audio quando il volume cambia.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE               | Descrizione                           |
|-----------------------|---------------------------------------|
| VT \_ EMPTY <br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene inviato dal flusso multimediale dell'origine di acquisizione audio.

L'origine di acquisizione audio invia questo evento se un'azione esterna modifica il volume, ad esempio se l'utente modifica il volume tramite il Pannello di controllo. L'origine di acquisizione non invia l'evento se l'applicazione modifica il volume direttamente nell'origine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                               |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




