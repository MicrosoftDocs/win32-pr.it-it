---
description: "Segnala un errore grave. Qualsiasi Media Foundation componente può inviare questo evento in qualsiasi momento. Chiamare IMFMediaEvent:: GetStatus per ottenere il codice di errore dell'operazione non riuscita."
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Evento MEError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb557dffb2c73a63031a193c331edabe470db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309640"
---
# <a name="meerror-event"></a>Evento MEError

Segnala un errore grave. Qualsiasi Media Foundation componente può inviare questo evento in qualsiasi momento. Chiamare [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) per ottenere il codice di errore dell'operazione non riuscita.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento deve essere utilizzato solo per gli errori imprevisti. Non inviare questo evento per segnalare che un metodo asincrono ha avuto esito negativo. Se un metodo asincrono ha esito negativo, il codice di errore viene restituito nell'evento normale per il metodo.

Se si verifica un errore reversibile durante il flusso, inviare l'evento [MENonFatalError](menonfatalerror.md) .

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

 

 




