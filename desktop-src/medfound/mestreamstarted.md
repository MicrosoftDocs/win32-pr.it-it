---
description: Generato da un flusso multimediale quando l'origine inizia senza eseguire la ricerca. Un flusso multimediale genera questo evento quando l'origine multimediale genera l'evento MESourceStarted.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Evento MEStreamStarted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a385516a6f0f973dd5bd0453d6c9751a0f7411a8ea43cb6acb936d8601c5272
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113941"
---
# <a name="mestreamstarted-event"></a>EVENTO MEStreamStarted

Generato da un flusso multimediale quando l'origine inizia senza eseguire la ricerca. Un flusso multimediale genera questo evento quando l'origine multimediale genera [l'evento MESourceStarted.](mesourcestarted.md)

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/>                                                                          |
| VT \_ I8<br/>    | Ora di inizio, in unità di 100 nanosecondi, rispetto ai timestamp nei campioni.<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




