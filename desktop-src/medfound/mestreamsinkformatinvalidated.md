---
description: Inviato da un sink di flusso quando il formato downstream è stato invalidato e deve essere rinegoziato.
ms.assetid: 732B3BDD-F394-430F-B895-AF18ED61114D
title: Evento MEStreamSinkFormatInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39c4453c0d5720ffb57f1277946f9cf891ed443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307992"
---
# <a name="mestreamsinkformatinvalidated-event"></a>Evento MEStreamSinkFormatInvalidated

Inviato da un sink di flusso quando il formato downstream è stato invalidato e deve essere rinegoziato.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

I dati accodati al sink, oltre la posizione di riproduzione corrente, devono essere inviati nuovamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                                      |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                                           |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




