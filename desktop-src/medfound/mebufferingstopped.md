---
description: Segnala che un'origine multimediale ha interrotto la memorizzazione dei dati nel buffer.
ms.assetid: 11b1290d-d462-4aa0-a358-b3f6447c99d8
title: Evento MEBufferingStopped (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e953ae5d7a79c04c33f4d0b4f9c87faa1e5798ed95d2d3bae29dbd0fab8b12a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878084"
---
# <a name="mebufferingstopped-event"></a>Evento MEBufferingStopped

Segnala che un'origine multimediale ha interrotto la memorizzazione dei dati nel buffer.

Un'origine multimediale lo invia quando interrompe la memorizzazione nel buffer dei dati dopo [l'invio dell'evento MEBufferingStarted.](mebufferingstarted.md)

Anche i flussi di byte che implementano [**l'interfaccia IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) inviano questo evento.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Quando la sessione multimediale riceve questo evento, riavvia l'orologio della presentazione. La sessione multimediale inoltra anche l'evento all'applicazione.

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

 

 




