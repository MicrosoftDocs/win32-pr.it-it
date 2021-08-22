---
description: Generato dalla sessione multimediale quando le funzionalità della sessione cambiano.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Evento MESessionCapabilitiesChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc97cb5168957f34cc029a982447c6d4775075ea6f9b9b250ce7b9fd7f1791d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464871"
---
# <a name="mesessioncapabilitieschanged-event"></a>Evento MESessionCapabilitiesChanged

Generato dalla sessione multimediale quando le funzionalità della sessione cambiano.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

L'evento contiene gli attributi seguenti.



| Attributo                                                                     | Descrizione                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [**MF \_ EVENT \_ SESSIONCAPS**](mf-event-sessioncaps-attribute.md)              | Nuovi flag di funzionalità della sessione.                  |
| [**MF \_ EVENT \_ SESSIONCAPS \_ DELTA**](mf-event-sessioncaps-delta-attribute.md) | Indica quali flag di funzionalità sono stati modificati. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




