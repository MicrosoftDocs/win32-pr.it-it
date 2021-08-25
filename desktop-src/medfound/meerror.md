---
description: Segnala un errore grave. Qualsiasi Media Foundation componente può inviare questo evento in qualsiasi momento. Chiamare IMFMediaEvent::GetStatus per ottenere il codice di errore dell'operazione non riuscita.
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Evento MEError (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd012bf7fbb7f21f37201a67f5c203f5981be6aa16795e2a3c37d16ea268f67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941471"
---
# <a name="meerror-event"></a>Evento MEError

Segnala un errore grave. Qualsiasi Media Foundation componente può inviare questo evento in qualsiasi momento. Chiamare [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) per ottenere il codice di errore dell'operazione non riuscita.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento deve essere usato solo per errori imprevisti. Non inviare questo evento per segnalare che un metodo asincrono non è riuscito. Se un metodo asincrono ha esito negativo, il codice di errore viene restituito nell'evento normale per tale metodo.

Se si verifica un errore ripristinabile durante lo streaming, inviare [l'evento MENonFatalError.](menonfatalerror.md)

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

 

 




