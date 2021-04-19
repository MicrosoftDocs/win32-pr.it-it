---
description: Generato da un sink del flusso quando completa una richiesta di ripulitura.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: Evento MEStreamSinkScrubSampleComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f29d478635d5a9ba7e7c5356c49ebd8da216f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318069"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a>Evento MEStreamSinkScrubSampleComplete

Generato da un sink del flusso quando completa una richiesta di ripulitura.

Lo scrubbing si verifica quando la velocità di riproduzione è zero e il clock di presentazione viene avviato con un tempo di srubbing specificato. Se un sink multimediale supporta lo scrubbing, ogni flusso del sink genera questo evento ogni volta che viene chiamato il metodo [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) mentre la velocità di riproduzione è zero.

Se il flusso esegue il rendering dei dati durante lo scrubbing, invia l'evento non appena viene eseguito il rendering dei dati. Se il flusso non esegue il rendering dei dati, invia l'evento immediatamente dopo la chiamata a [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) .

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                              | Descrizione                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tempo di \_ SCRUBSAMPLE \_ evento MF**](mf-event-scrubsample-time-attribute.md)<br/> | Tempo di presentazione per cui è stato eseguito il rendering dei dati. Se il sink multimediale non esegue il rendering dei dati durante lo scrubbing, questo attributo non viene impostato.<br/> <br/> |



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

[Sink di supporti](media-sinks.md)
</dt> <dt>

[MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




