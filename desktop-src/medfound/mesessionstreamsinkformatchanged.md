---
description: Generato dalla sessione multimediale quando il formato viene modificato in un sink multimediale.
ms.assetid: f56419f8-7f50-4eda-bf4a-fcdbbe46e180
title: Evento MESessionStreamSinkFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed59b9600cbaf8cb942a42beb6bed46d62fc15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226657"
---
# <a name="mesessionstreamsinkformatchanged-event"></a>Evento MESessionStreamSinkFormatChanged

Generato dalla sessione multimediale quando il formato viene modificato in un sink multimediale.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                    | Descrizione                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_nodo di \_ output \_ evento MF**](mf-event-output-node-attribute.md)<br/> | Identifica il nodo della topologia per il sink multimediale il cui formato è stato modificato.<br/> <br/> |



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

 

 




