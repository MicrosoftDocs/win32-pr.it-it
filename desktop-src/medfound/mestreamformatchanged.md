---
description: Generato da un flusso multimediale quando cambia il tipo di supporto del flusso.
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: Evento MEStreamFormatChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762f65beb26f5095c9e89be845f468e3ca53c9b5cd227916bb7cc38417626c60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957271"
---
# <a name="mestreamformatchanged-event"></a>Evento MEStreamFormatChanged

Generato da un flusso multimediale quando cambia il tipo di supporto del flusso.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Puntatore [**all'interfaccia IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) del nuovo tipo di supporto.<br/> <br/> |



## <a name="remarks"></a>Commenti

Usare questo evento per segnalare le modifiche al formato nel flusso.

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

 

 




