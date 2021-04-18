---
description: Generato dalla sessione multimediale all'avvio di una nuova presentazione. Questo evento indica quando verrà avviata la presentazione e l'offset tra l'ora di presentazione e l'ora di origine.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: Evento MESessionNotifyPresentationTime (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b0cd8811d98094ab58ddcf844ec73e1470d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309614"
---
# <a name="mesessionnotifypresentationtime-event"></a>Evento MESessionNotifyPresentationTime

Generato dalla sessione multimediale all'avvio di una nuova presentazione. Questo evento indica quando verrà avviata la presentazione e l'offset tra l'ora di presentazione e l'ora di origine.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                                                                   | Descrizione                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**\_ora di \_ presentazione di inizio evento \_ MF \_**](mf-event-start-presentation-time-attribute.md)<br/>                       | Ora di inizio della presentazione.<br/> <br/>                                                      |
| [**\_ \_ \_ offset ora presentazione evento \_ MF**](mf-event-presentation-time-offset-attribute.md)<br/>                     | Offset tra l'ora di presentazione e i timestamp dell'origine multimediale.<br/> <br/>                 |
| [**\_ \_ \_ \_ ora di presentazione dell'avvio \_ dell'evento MF nell' \_ output**](mf-event-start-presentation-time-at-output-attribute.md)<br/> | Tempo di presentazione quando i sink del supporto eseguiranno il rendering del primo campione della nuova topologia.<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




