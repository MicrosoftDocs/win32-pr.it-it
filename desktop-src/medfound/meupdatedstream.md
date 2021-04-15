---
description: Generato da un'origine multimediale quando viene riavviato o Cerca un flusso già attivo.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Evento MEUpdatedStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3b2e6fdc5928a08306b344c02b5eaafc37e957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529604"
---
# <a name="meupdatedstream-event"></a>Evento MEUpdatedStream

Generato da un'origine multimediale quando viene riavviato o Cerca un flusso già attivo.

Quando il metodo [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) viene chiamato su un'origine multimediale, l'origine multimediale Invia un evento per ogni flusso selezionato:

-   L'origine invia l'evento [MENewStream](menewstream.md) se il flusso non è stato selezionato nella precedente chiamata a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)oppure si tratta della prima chiamata **iniziale** a questa origine multimediale.

-   L'origine invia l'evento MEUpdatedStream se il flusso è già stato selezionato nella precedente chiamata a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

Non viene inviato alcun evento per i flussi non selezionati.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| VT \_ sconosciuto<br/> | Puntatore all'interfaccia [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) del flusso.<br/> <br/> |



## <a name="remarks"></a>Commenti

Alla prima chiamata a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) in cui un flusso diventa attivo, l'origine multimediale Invia un evento [MENewStream](menewstream.md) per il flusso. Nelle chiamate successive a **Start**, l'origine multimediale Invia un evento MEUpdatedStream, finché il flusso non viene deselezionato.

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

 

 




