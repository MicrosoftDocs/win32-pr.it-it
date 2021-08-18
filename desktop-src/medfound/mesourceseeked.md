---
description: Generato quando un'origine multimediale cerca in una nuova posizione. Un'origine multimediale genera questo evento se l'origine è in esecuzione o sospesa e l'applicazione chiama IMFMediaSource::Start con un'ora di inizio non uguale alla posizione corrente.
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: Evento MESourceSeeked (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b913089ca40895a782f3c013b752db25fe754443ae6d79b410da98e759b4b8ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941411"
---
# <a name="mesourceseeked-event"></a>EVENTO MESourceSeeked

Generato quando un'origine multimediale cerca in una nuova posizione. Un'origine multimediale genera questo evento se l'origine è in esecuzione o sospesa e l'applicazione chiama [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) con un'ora di inizio non uguale alla posizione corrente.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE           | Descrizione                                                                |
|-------------------|----------------------------------------------------------------------------|
| VT \_ I8<br/> | Nuova posizione iniziale, in unità di 100 nanosecondi.<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




