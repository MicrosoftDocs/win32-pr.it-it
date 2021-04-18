---
description: Generato dalla sessione multimediale quando le funzionalità della sessione cambiano.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Evento MESessionCapabilitiesChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0612b705571c50a6adcbde4afe93b42a524a950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309617"
---
# <a name="mesessioncapabilitieschanged-event"></a>Evento MESessionCapabilitiesChanged

Generato dalla sessione multimediale quando le funzionalità della sessione cambiano.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

L'evento contiene gli attributi seguenti.



| Attributo                                                                     | Descrizione                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [**\_SESSIONCAPS evento \_ MF**](mf-event-sessioncaps-attribute.md)              | Nuovi flag delle funzionalità della sessione.                  |
| [**\_ \_ Delta SESSIONCAPS evento \_ MF**](mf-event-sessioncaps-delta-attribute.md) | Indica quali flag delle funzionalità sono stati modificati. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




