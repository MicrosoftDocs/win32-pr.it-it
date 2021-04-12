---
description: Segnala che un'origine multimediale ha interrotto l'inserimento dei dati nel buffer.
ms.assetid: 11b1290d-d462-4aa0-a358-b3f6447c99d8
title: Evento MEBufferingStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e996ec160f57ec598196b388170741705adb9a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344301"
---
# <a name="mebufferingstopped-event"></a>Evento MEBufferingStopped

Segnala che un'origine multimediale ha interrotto l'inserimento dei dati nel buffer.

Un'origine multimediale Invia questo elemento quando interrompe il buffering dei dati dopo l'invio dell'evento [MEBufferingStarted](mebufferingstarted.md) .

Anche i flussi di byte che implementano l'interfaccia [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) inviano questo evento.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Quando la sessione multimediale riceve questo evento, riavvia il clock di presentazione. La sessione multimediale trasmette inoltre l'evento all'applicazione.

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

 

 




