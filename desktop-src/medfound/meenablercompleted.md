---
description: Generato da un oggetto Enabler del contenuto quando viene completata l'azione di abilitazione degli oggetti.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Evento MEEnablerCompleted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a74f7379ccc2983abd2327e1250bcf1ca14e688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130746"
---
# <a name="meenablercompleted-event"></a>Evento MEEnablerCompleted

Generato da un oggetto Enabler del contenuto quando l'azione di abilitazione dell'oggetto viene completata. Gli oggetti che espongono l'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) possono generare questo evento. L'evento viene generato se si verifica una delle condizioni seguenti:

-   Il metodo [**IMFContentEnabler:: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) viene completato in modo asincrono.
-   Tramite l'applicazione viene chiamato [**IMFContentEnabler:: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), quindi l'applicazione completa la richiesta HTTP post, come descritto nel metodo **MonitorEnable** .

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Il codice di stato dell'evento può contenere uno dei valori seguenti.



|                                      |                                                                                                                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_OK**                            | Operazione completata.                                                                                                                                                        |
| **NS \_ E \_ DRM \_ License \_ NOTACQUIRED** | La licenza DRM non è stata acquisita. Se il tentativo precedente usava [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), l'applicazione dovrebbe provare a eseguire un'acquisizione non invisibile all'utente. |
| **\_monitoraggio DRM di NS è stato \_ \_ \_ annullato**   | L'operazione [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) è stata annullata.                                                                                            |



 

Per ricevere questo evento, eseguire una query sull'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) per l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Chiamare quindi [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), come descritto nell'argomento [generatori di eventi multimediali](media-event-generators.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Generatori di eventi multimediali](media-event-generators.md)
</dt> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




