---
description: Generato da un oggetto di abilitazione del contenuto quando l'azione di abilitazione degli oggetti viene completata.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Evento MEEnablerCompleted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f05459a648f6b357fd483baa9fc56809540e64a1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119446"
---
# <a name="meenablercompleted-event"></a>Evento MEEnablerCompleted

Generato da un oggetto content enabler quando viene completata l'azione di abilitazione dell'oggetto. Gli oggetti che espongono [**l'interfaccia IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) possono generare questo evento. L'evento viene generato se si verifica una delle condizioni seguenti:

-   Il [**metodo IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) viene completato in modo asincrono.
-   L'applicazione chiama [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)e quindi l'applicazione completa la richiesta HTTP POST, come descritto nel **metodo MonitorEnable.**

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Il codice di stato dell'evento può contenere uno dei valori seguenti.



| Valore                                     | Descrizione                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **S \_ OK**                            | Operazione completata.                                                                                                                                                        |
| **LICENZA \_ NS E \_ DRM \_ NON \_ RICHIESTA** | La licenza DRM non è stata acquisita. Se il tentativo precedente usa [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), l'applicazione deve provare l'acquisizione non invisibile all'utente. |
| **MONITORAGGIO \_ \_ DRM S \_ NS \_ ANNULLATO**   | [**L'operazione MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) è stata annullata.                                                                                            |



 

Per ricevere questo evento, eseguire una query [**sull'interfaccia IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) per [**l'interfaccia IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Chiamare quindi [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), come descritto nell'argomento [Generatori di eventi multimediali](media-event-generators.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                                           |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Generatori di eventi multimediali](media-event-generators.md)
</dt> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




