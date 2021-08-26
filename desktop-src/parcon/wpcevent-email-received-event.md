---
description: Evento per utente generato da un client di posta elettronica quando si tenta di ricevere un messaggio in Controllo genitori.
ms.assetid: 3b8d9bac-16b0-49e9-b360-b2d6e82f1753
title: WPCEVENT_EMAIL_RECEIVED eventi (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81a51e79125403504aae2ed6e823c10044ffc35ed36ff139e8333f955338d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951561"
---
# <a name="wpcevent_email_received-event"></a>Evento WPCEVENT \_ EMAIL \_ RECEIVED

Evento per utente generato da un client di posta elettronica quando si tenta di ricevere un messaggio in Controllo genitori.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_RECEIVED = {0x4, 0x0, 0x10, 0x4, 0x16, 0x4, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Mittente* 
</dt> <dd>

Nome dell'account di posta elettronica dell'entità mittente.

</dd> <dt>

*AppName* 
</dt> <dd>

Nome dell'applicazione di posta elettronica che genera l'evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Versione dell'applicazione di posta elettronica che genera l'evento.

</dd> <dt>

*Oggetto* 
</dt> <dd>

Riga dell'oggetto del messaggio ricevuto.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore [**dell'enumerazione WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) che indica informazioni sugli eventi che non possono essere utilizzati e sui controlli presenti.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Numero di indirizzi di posta elettronica che ricevono il messaggio e che dispongono di identità definite nel campo destinatario.

</dd> <dt>

*Recipient* 
</dt> <dd>

Stringa delimitata che contiene i nomi degli account di posta elettronica di tutti i destinatari del messaggio.

</dd> <dt>

*AttachCount* 
</dt> <dd>

Numero di allegati al messaggio.

</dd> <dt>

*AttachmentName* 
</dt> <dd>

Stringa delimitata che contiene i nomi di tutti gli allegati al messaggio.

</dd> <dt>

*ReceivedTime* 
</dt> <dd>

Ora in cui è stato tentato di ricevere il messaggio.

</dd> <dt>

*EmailAccount* 
</dt> <dd>

Nome dell'account di posta elettronica per l'utente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso delle API di registrazione per il controllo genitori](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




