---
description: Generato da un sink di flusso quando completa una richiesta di scrubbing.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: Evento MEStreamSinkScrubSampleComplete (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ae6e0ea7a90db33fe21d39017ac99908ace86bb263e0ad6e2047f70e70f5de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715171"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a>Evento MEStreamSinkScrubSampleComplete

Generato da un sink di flusso quando completa una richiesta di scrubbing.

Lo scrubbing si verifica quando la velocità di riproduzione è zero e l'orologio della presentazione viene avviato con un'ora di scorrimento specificata. Se un sink multimediale supporta lo scrubbing, ogni flusso sul sink genera questo evento ogni volta che viene chiamato il metodo [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) mentre la velocità di riproduzione è zero.

Se il flusso esegue il rendering dei dati durante lo scrubbing, invia l'evento non appena viene eseguito il rendering dei dati. Se il flusso non esegue il rendering dei dati, invia l'evento immediatamente dopo la chiamata a [**OnClockStart.**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                              | Descrizione                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TEMPO DI \_ \_ SCRUBSAMPLE DELL'EVENTO MF \_**](mf-event-scrubsample-time-attribute.md)<br/> | Ora di presentazione per cui è stato eseguito il rendering dei dati. Se il sink multimediale non esegue il rendering dei dati durante lo scrubbing, non imposta questo attributo.<br/> <br/> |



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

[Sink di supporti](media-sinks.md)
</dt> <dt>

[MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




