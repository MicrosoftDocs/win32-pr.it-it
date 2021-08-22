---
description: Generato dalla sessione multimediale quando completa una richiesta di pulitura.
ms.assetid: 1ae97022-3fb2-4c5e-9262-d5bdc2a62bee
title: Evento MESessionScrubSampleComplete (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2fdaa6ffe9693fc6a033fd0c33ff519a73dcda3a32c303844da04e6af01404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974175"
---
# <a name="mesessionscrubsamplecomplete-event"></a>EVENTO MESessionScrubSampleComplete

Generato dalla sessione multimediale quando completa una richiesta di pulitura.

Lo scrubbing si verifica quando la frequenza di riproduzione è zero e l'applicazione chiama [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). Questo evento viene generato dopo che ogni sink di flusso ha completato la richiesta di pulitura.

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

[MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md)
</dt> </dl>

 

 




