---
description: Generato da un sink di flusso per richiedere un nuovo esempio multimediale dalla pipeline.
ms.assetid: 35020a15-942f-4dd0-9ca4-815affdacecf
title: Evento MEStreamSinkRequestSample (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de147486f54485ecb9f80b15394b1a2d48021c1f602ccd138cf6718ef7ec2c0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061326"
---
# <a name="mestreamsinkrequestsample-event"></a>EVENTO MEStreamSinkRequestSample

Generato da un sink di flusso per richiedere un nuovo esempio multimediale dalla pipeline. Per ogni evento MEStreamSinkRequestSample, la pipeline richiede i dati dal componente upstream successivo.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



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

[Sink multimediali](media-sinks.md)
</dt> </dl>

 

 




