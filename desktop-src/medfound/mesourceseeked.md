---
description: "Generato quando un'origine multimediale cerca una nuova posizione. Un'origine multimediale genera questo evento se l'origine è in esecuzione o in pausa e l'applicazione chiama IMFMediaSource:: Start con un'ora di inizio che non corrisponde alla posizione corrente."
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: Evento MESourceSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589e6619b4b4147da65a327681ad4ed2eace89c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308003"
---
# <a name="mesourceseeked-event"></a>Evento MESourceSeeked

Generato quando un'origine multimediale cerca una nuova posizione. Un'origine multimediale genera questo evento se l'origine è in esecuzione o in pausa e l'applicazione chiama [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) con un'ora di inizio che non corrisponde alla posizione corrente.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE           | Descrizione                                                                |
|-------------------|----------------------------------------------------------------------------|
| \_I8 VT<br/> | Nuova posizione iniziale, in unità di 100 nanosecondi.<br/> <br/> |



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

 

 




