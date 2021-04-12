---
description: Si è verificato un errore non irreversibile durante il flusso.
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: Evento MENonFatalError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6af26a87b99e9c2ef649684c4ede53e707e7084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344621"
---
# <a name="menonfatalerror-event"></a>Evento MENonFatalError

Si è verificato un errore non irreversibile durante il flusso. Qualsiasi Media Foundation componente può inviare questo evento in qualsiasi momento.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE            | Descrizione                                                        |
|--------------------|--------------------------------------------------------------------|
| \_UI4 VT<br/> | Valore **HRESULT** che descrive l'errore.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento non sono definiti attributi.

## <a name="remarks"></a>Commenti

Questo evento segnala un errore imprevisto ma reversibile durante il flusso. Ad esempio, un'origine multimediale può inviare questo evento se elimina un pacchetto.

Non inviare questo evento per segnalare che un metodo asincrono ha avuto esito negativo. Se un metodo asincrono ha esito negativo, il codice di errore viene restituito nell'evento normale per il metodo.

Se si verifica un errore di streaming non reversibile, inviare l'evento [MEError](meerror.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




