---
description: Generato da un'autorità di attendibilità di output quando il metodo IMFOutputTrustAuthority::SetPolicy viene completato in modo asincrono.
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: Evento MEPolicySet (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064cbb92e85e300aa2c2b7db28d08b01296834413ed92e36eb5b7ce88e5486c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877558"
---
# <a name="mepolicyset-event"></a>EVENTO MEPolicySet

Generato da un'autorità di attendibilità di output quando il [**metodo IMFOutputTrustAuthority::SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) viene completato in modo asincrono.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |
| VT \_ UI4<br/> | Identificatore che può essere impostato su un [oggetto IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) tramite l MF_POLICY_ID attribuito . [](mf-policy-id.md)<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




