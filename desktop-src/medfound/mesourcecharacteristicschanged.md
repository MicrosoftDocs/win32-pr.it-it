---
description: Generato da un'origine multimediale quando le caratteristiche delle origini cambiano.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: Evento MESourceCharacteristicsChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd69be00727ec3f1f635b82fb6c8e29c4016959ced480be4e9de6b8a83cfe8cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877369"
---
# <a name="mesourcecharacteristicschanged-event"></a>EVENTO MESourceCharacteristicsChanged

Generato da un'origine multimediale quando le caratteristiche dell'origine cambiano.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                                                   | Descrizione                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**CARATTERISTICHE \_ DELL'ORIGINE EVENTO MF \_ \_**](mf-event-source-characteristics-attribute.md)<br/>          | Nuove caratteristiche dell'origine multimediale.<br/> <br/>      |
| [**CARATTERISTICHE \_ DELL'ORIGINE EVENTO MF \_ \_ \_ PRECEDENTE**](mf-event-source-characteristics-old-attribute.md)<br/> | Caratteristiche precedenti dell'origine multimediale.<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




