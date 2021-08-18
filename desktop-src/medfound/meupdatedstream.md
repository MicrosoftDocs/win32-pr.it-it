---
description: Generato da un'origine multimediale al riavvio o alla ricerca di un flusso già attivo.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Evento MEUpdatedStream (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5746b619f885ab7648110cbe58b66b7897c839031202d811becd33e1c84991a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974020"
---
# <a name="meupdatedstream-event"></a>Evento MEUpdatedStream

Generato da un'origine multimediale al riavvio o alla ricerca di un flusso già attivo.

Quando il [**metodo IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) viene chiamato su un'origine multimediale, l'origine multimediale invia un evento per ogni flusso selezionato:

-   L'origine invia l'evento [MENewStream](menewstream.md) se il flusso non è stato selezionato nella chiamata precedente a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)o se si tratta della prima chiamata a **Start** in questa origine multimediale.

-   L'origine invia l'evento MEUpdatedStream se il flusso è già stato selezionato nella chiamata precedente a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

Non viene inviato alcun evento per i flussi non selezionati.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Puntatore all'interfaccia [**IMFMediaStream del**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) flusso.<br/> <br/> |



## <a name="remarks"></a>Commenti

Alla prima chiamata a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) in cui un flusso diventa attivo, l'origine multimediale invia un [evento MENewStream](menewstream.md) per il flusso. Nelle chiamate successive a **Start,** l'origine multimediale invia un evento MEUpdatedStream fino a quando il flusso non viene deselezionato.

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

 

 




