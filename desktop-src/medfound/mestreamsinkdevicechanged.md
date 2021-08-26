---
description: Generato dai sink di flusso del renderer video avanzato (EVR) se il dispositivo video viene modificato.
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: Evento MEStreamSinkDeviceChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb760a45125ae7434ff2a58d43f087d2ec3c030cb29351ea4d2113ca8fe10c0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061011"
---
# <a name="mestreamsinkdevicechanged-event"></a>EVENTO MEStreamSinkDeviceChanged

Generato dai sink di flusso del renderer video avanzato (EVR) se il dispositivo video viene modificato. Ad esempio, l'EVR genera questo evento quando riceve un [**evento EC \_ DISPLAY \_ CHANGED.**](../directshow/ec-display-changed.md)

La pipeline Media Foundation risponde a questo evento inviando nuovamente tutte le richieste di esempio non riuscite durante la modifica del dispositivo.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> <dt>

[Sink multimediali](media-sinks.md)
</dt> </dl>

 

 
