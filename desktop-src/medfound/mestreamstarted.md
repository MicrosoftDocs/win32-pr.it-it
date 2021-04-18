---
description: Generato da un flusso multimediale quando l'origine viene avviata senza la ricerca. Un flusso multimediale genera questo evento quando l'origine multimediale genera l'evento MESourceStarted.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Evento MEStreamStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479726c1295b4497080b2e15abdde1558f0d4888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309604"
---
# <a name="mestreamstarted-event"></a>Evento MEStreamStarted

Generato da un flusso multimediale quando l'origine viene avviata senza la ricerca. Un flusso multimediale genera questo evento quando l'origine multimediale genera l'evento [MESourceStarted](mesourcestarted.md) .

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/>                                                                          |
| \_I8 VT<br/>    | Ora di inizio, in unità di 100 nanosecondi, relativa ai timestamp degli esempi.<br/> <br/> |



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

 

 




