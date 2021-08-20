---
description: Generato dalla sessione multimediale all'avvio di una nuova presentazione. Questo evento indica quando verrà avviata la presentazione e l'offset tra l'ora di presentazione e l'ora di origine.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: Evento MESessionNotifyPresentationTime (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10c1b1e443bd2c6a56a926d5355de5606bf2f2e25618269f8d4ed735538d92f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061765"
---
# <a name="mesessionnotifypresentationtime-event"></a>EVENTO MESessionNotifyPresentationTime

Generato dalla sessione multimediale all'avvio di una nuova presentazione. Questo evento indica quando verrà avviata la presentazione e l'offset tra l'ora di presentazione e l'ora di origine.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                                                                   | Descrizione                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**ORA DI INIZIO \_ PRESENTAZIONE \_ \_ DELL'EVENTO \_ MF**](mf-event-start-presentation-time-attribute.md)<br/>                       | Ora di inizio della presentazione.<br/> <br/>                                                      |
| [**OFFSET \_ DELL'ORA \_ DI PRESENTAZIONE \_ DELL'EVENTO \_ MF**](mf-event-presentation-time-offset-attribute.md)<br/>                     | Offset tra l'ora di presentazione e i timestamp dell'origine multimediale.<br/> <br/>                 |
| [**ORA DI INIZIO PRESENTAZIONE DELL'EVENTO MF \_ \_ \_ \_ \_ \_ ALL'OUTPUT**](mf-event-start-presentation-time-at-output-attribute.md)<br/> | Ora di presentazione in cui i sink multimediali eseguiranno il rendering del primo esempio della nuova topologia.<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




