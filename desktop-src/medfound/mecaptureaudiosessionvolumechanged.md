---
description: Inviato da un'origine di acquisizione audio quando cambia il volume.
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: Evento MECaptureAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a391c55e8fcebaef0f620430b12f7cdcc67364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308473"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a>Evento MECaptureAudioSessionVolumeChanged

Inviato da un'origine di acquisizione audio quando cambia il volume.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE               | Descrizione                           |
|-----------------------|---------------------------------------|
| VT \_ vuoto <br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene inviato dal flusso multimediale dell'origine di acquisizione audio.

L'origine di acquisizione audio Invia questo evento se un'azione esterna modifica il volume, ad esempio se l'utente modifica il volume tramite il pannello di controllo. L'origine di acquisizione non invia l'evento se l'applicazione modifica il volume direttamente nell'origine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




