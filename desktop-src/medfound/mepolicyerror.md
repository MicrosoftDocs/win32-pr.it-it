---
description: Generato da un output attendibile se si verifica un errore durante l'applicazione dei criteri di output.
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: Evento MEPolicyError (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce1f0d05b73ea295ea3282af5950d4a9a61f833f61463cd095848563e3858c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877548"
---
# <a name="mepolicyerror-event"></a>EVENTO MEPolicyError

Generato da un output attendibile se si verifica un errore durante l'applicazione dei criteri di output.

Se la sessione multimediale riceve questo evento, interrompe la riproduzione e inoltra l'evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

I valori possibili recuperati [**da IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) includono quanto segue.



| Valore                      | Descrizione                                                    |
|----------------------------|----------------------------------------------------------------|
| CRITERI DI MF \_ E \_ NON \_ SUPPORTATI | L'output attendibile non supporta i criteri di output correnti. |



 

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

 

 




