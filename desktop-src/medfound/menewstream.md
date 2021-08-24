---
description: Generato da un'origine multimediale all'avvio di un nuovo flusso.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Evento MENewStream (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499b7899c499e87a45e9b7f043db94724b41d729d3b836e7c9f8d71d83616841
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228771"
---
# <a name="menewstream-event"></a>EVENTO MENewStream

Generato da un'origine multimediale all'avvio di un nuovo flusso.

Quando il [**metodo IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) viene chiamato su un'origine multimediale, l'origine multimediale invia un evento per ogni flusso selezionato:

-   L'origine invia l'evento MENewStream se il flusso non è stato selezionato nella chiamata precedente a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)o se si tratta della prima chiamata a **Start** su questa origine multimediale.

-   L'origine invia [l'evento MEUpdatedStream](meupdatedstream.md) se il flusso è già stato selezionato nella chiamata precedente a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

Non viene inviato alcun evento per i flussi non selezionati.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Contiene un puntatore [**all'interfaccia IMFMediaStream del**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) flusso.<br/> <br/> |



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

 

 




