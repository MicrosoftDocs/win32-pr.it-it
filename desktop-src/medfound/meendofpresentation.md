---
description: Generato da un'origine multimediale al termine di una presentazione. Questo evento segnala che tutti i flussi nella presentazione sono completi. La sessione multimediale inoltra questo evento all'applicazione.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: Evento MEEndOfPresentation (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e97a2689b8d0e2ae156daa84f27f0e10fb31b828ffedf027a7be47a6c330b7b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941461"
---
# <a name="meendofpresentation-event"></a>Evento MEEndOfPresentation

Generato da un'origine multimediale al termine di una presentazione. Questo evento segnala che tutti i flussi nella presentazione sono completi. La sessione multimediale inoltra questo evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                                               | Descrizione                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**TOPOLOGIA \_ \_ DELL'ORIGINE \_ EVENTO MF \_ ANNULLATA**](mf-event-source-topology-canceled-attribute.md)<br/> | Specifica se l'origine sequencer ha annullato la presentazione.<br/> <br/> |



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

 

 




