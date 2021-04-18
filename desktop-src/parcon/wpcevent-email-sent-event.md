---
description: Evento per utente generato da un client di posta elettronica quando si tenta di inviare un messaggio nei controlli padre.
ms.assetid: c49919a2-2a03-475d-9cfa-20a960184202
title: Evento WPCEVENT_EMAIL_SENT (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd222e946f0b7c78116ace9d8d01de2e2709a7ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318391"
---
# <a name="wpcevent_email_sent-event"></a>\_Evento WPCEVENT inviato tramite posta elettronica \_

Evento per utente generato da un client di posta elettronica quando si tenta di inviare un messaggio nei controlli padre.


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

Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Numero degli indirizzi di posta elettronica che ricevono il messaggio e che hanno identità definite nel campo del destinatario.

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

Data e ora in cui è stato tentato di ricevere il messaggio.

</dd> <dt>

*EmailAccount* 
</dt> <dd>

Nome dell'account di posta elettronica per l'utente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso delle API di registrazione per i controlli padre](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**\_argomenti \_ CONVERSATIONINITEVENT di WPC**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




