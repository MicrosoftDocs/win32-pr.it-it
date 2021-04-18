---
description: Generato da un'origine multimediale quando avvia un nuovo flusso.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Evento MENewStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60394d442b24dcdc234ada2dd3fd418e6ab7b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309630"
---
# <a name="menewstream-event"></a>Evento MENewStream

Generato da un'origine multimediale quando avvia un nuovo flusso.

Quando il metodo [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) viene chiamato su un'origine multimediale, l'origine multimediale Invia un evento per ogni flusso selezionato:

-   L'origine invia l'evento MENewStream se il flusso non è stato selezionato nella precedente chiamata a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)oppure si tratta della prima chiamata **iniziale** a questa origine multimediale.

-   L'origine invia l'evento [MEUpdatedStream](meupdatedstream.md) se il flusso è già stato selezionato nella precedente chiamata a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

Non viene inviato alcun evento per i flussi non selezionati.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| VT \_ sconosciuto<br/> | Contiene un puntatore all'interfaccia [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) del flusso.<br/> <br/> |



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

 

 




