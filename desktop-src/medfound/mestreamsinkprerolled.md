---
description: Generato da un sink di flusso quando il flusso ha ricevuto dati di pre-roll sufficienti per avviare il rendering. Questo evento viene generato da sink multimediali che supportano l'interfaccia IMFMediaSinkPreroll.
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: Evento MEStreamSinkPrerolled (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d46c4c4e076651cb38318bb908df280c503c0880a256087f4192433ecdb5406a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464801"
---
# <a name="mestreamsinkprerolled-event"></a>Evento MEStreamSinkPrerolled

Generato da un sink di flusso quando il flusso ha ricevuto dati di pre-roll sufficienti per avviare il rendering. Questo evento viene generato da sink multimediali che supportano [**l'interfaccia IMFMediaSinkPreroll.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll)

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> <dt>

[Sink di supporti](media-sinks.md)
</dt> </dl>

 

 




