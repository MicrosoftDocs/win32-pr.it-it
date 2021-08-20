---
description: Generato da un flusso multimediale dopo una chiamata a IMFMediaSource::Start causa una ricerca nel flusso. Un flusso multimediale genera questo evento quando l'origine multimediale genera l'evento MESourceSeeked.
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: Evento MEStreamSeeked (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b03e58b11785a7b807f6793ff2ba6b2a4afa5f912d21e626938d7b3c725242f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061336"
---
# <a name="mestreamseeked-event"></a>Evento MEStreamSeeked

Generato da un flusso multimediale dopo una chiamata a [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causa una ricerca nel flusso. Un flusso multimediale genera questo evento quando l'origine multimediale genera [l'evento MESourceSeeked.](mesourceseeked.md)

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE           | Descrizione                                                        |
|-------------------|--------------------------------------------------------------------|
| VT \_ I8<br/> | Nuova ora di inizio, in unità da 100 nanosecondi.<br/> <br/> |



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

 

 




