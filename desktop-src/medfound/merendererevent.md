---
description: Segnala un evento da un sink multimediale che esegue il rendering dei dati multimediali.
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: Evento MERendererEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e15bfbe97743e8af10a79cf3ef1d94626a877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226660"
---
# <a name="merendererevent-event"></a>Evento MERendererEvent

Segnala un evento da un sink multimediale che esegue il rendering dei dati multimediali.

Il [renderer video avanzato](enhanced-video-renderer.md) (EVR) Invia questo evento quando riceve un evento utente dal Presenter di EVR.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE           | Descrizione                        |
|-------------------|------------------------------------|
| VT \_ I4<br/> | Codice evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Se il relatore chiama il metodo **IMediaEventSink:: Notify** di EVR con un codice evento nell'intervallo EC \_ utente o superiore, EVR Invia questo evento. I dati dell'evento sono il codice evento passato al metodo **Notify** .

I parametri dell'evento originale (*EventParam1* e *EventParam2* nel metodo **IMediaEventSink:: Notify** ) vengono ignorati, quindi il Presenter deve impostare questi valori su **null**.

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

 

 




