---
description: Evento per utente generato da un client di posta elettronica quando si tenta di inviare un messaggio in Controllo genitori.
ms.assetid: c49919a2-2a03-475d-9cfa-20a960184202
title: WPCEVENT_EMAIL_SENT evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe3d5fb08764aa83677fcca66af7f1e3b868f2b1bdf393741865bf64fd23049
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112731"
---
# <a name="wpcevent_email_sent-event"></a>Evento WPCEVENT \_ EMAIL \_ SENT

Evento per utente generato da un client di posta elettronica quando si tenta di inviare un messaggio in Controllo genitori.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_SENT = {0x5, 0x0, 0x10, 0x4, 0x16, 0x5, 0x8000000000000030};
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

Valore [**dell'enumerazione WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) che indica quali eventi non possono essere utilizzati e quali controlli sono presenti.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Numero di destinatari di posta elettronica che ricevono il messaggio e che dispongono di identità definite nel campo del destinatario.

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
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso delle API di registrazione per Controllo genitori](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




