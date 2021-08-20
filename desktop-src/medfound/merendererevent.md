---
description: Segnala un evento da un sink multimediale che esegue il rendering dei dati multimediali.
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: Evento MERendererEvent (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9fc70505033b9d88cd9593d2efa9f3c591f69f5e25bd968b06686c4c6ac911d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061856"
---
# <a name="merendererevent-event"></a>EVENTO MERendererEvent

Segnala un evento da un sink multimediale che esegue il rendering dei dati multimediali.

Il [renderer video avanzato](enhanced-video-renderer.md) (EVR) invia questo evento quando riceve un evento utente dal presentatore EVR.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE           | Descrizione                        |
|-------------------|------------------------------------|
| VT \_ I4<br/> | Codice evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Se il presentatore chiama il metodo **IMediaEventSink::Notify** di EVR con un codice evento compreso nell'intervallo EC USER o \_ superiore, l'EVR invia questo evento. I dati dell'evento sono il codice evento passato al **metodo Notify.**

I parametri dell'evento originale (*EventParam1* ed *EventParam2* nel metodo **IMediaEventSink::Notify)** vengono ignorati, quindi il presentatore deve impostare questi valori su **NULL.**

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

 

 




