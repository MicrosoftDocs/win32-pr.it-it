---
description: Generato dall'origine sequencer quando un segmento viene completato ed è seguito da un altro segmento. Quando il segmento finale viene completato, l'origine sequencer genera un evento MEEndOfPresentation.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Evento MEEndOfPresentationSegment (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b82f646ca76dbb6cc3cd8dc9e95dbaca2c55c504af261924918dbf790411e7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013701"
---
# <a name="meendofpresentationsegment-event"></a>EVENTO MEEndOfPresentationSegment

Generato dall'origine sequencer quando un segmento viene completato ed è seguito da un altro segmento. Quando il segmento finale viene completato, l'origine sequencer genera un [evento MEEndOfPresentation.](meendofpresentation.md)

La sessione multimediale inoltra questo evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                                               | Descrizione                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**TOPOLOGIA \_ DELL'ORIGINE EVENTO MF \_ \_ \_ ANNULLATA**](mf-event-source-topology-canceled-attribute.md)<br/> | Specifica se l'origine sequencer ha annullato questo segmento.<br/> <br/> |



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

[Informazioni sull'origine Sequencer](about-the-sequencer-source.md)
</dt> <dt>

[Eventi di origine sequencer](sequencer-source-events.md)
</dt> </dl>

 

 




