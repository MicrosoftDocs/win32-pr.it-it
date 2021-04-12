---
description: Evento per utente generato da un client di posta elettronica che registra quando viene aggiunto, modificato o eliminato un contatto nei controlli padre.
ms.assetid: 9d1f52ef-ff49-4c0d-a48a-93aeccbe7f2b
title: Evento WPCEVENT_EMAIL_CONTACT (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0974030e53756b44f2be2e8550707161f2d6d461
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233734"
---
# <a name="wpcevent_email_contact-event"></a>\_Evento di contatto di posta elettronica WPCEVENT \_

Evento per utente generato da un client di posta elettronica che registra quando viene aggiunto, modificato o eliminato un contatto nei controlli padre.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_CONTACT = {0xe, 0x0, 0x10, 0x4, 0x16, 0xe, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AppName* 
</dt> <dd>

Nome dell'applicazione di posta elettronica che genera l'evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Versione dell'applicazione di posta elettronica che genera l'evento.

</dd> <dt>

*OldName* 
</dt> <dd>

Nome dell'account di posta elettronica precedente, se eliminato o modificato.

</dd> <dt>

*OldID* 
</dt> <dd>

ID associato al nome dell'account di posta elettronica precedente.

</dd> <dt>

*NewName* 
</dt> <dd>

Nome del nuovo account di posta elettronica, se aggiunto o modificato.

</dd> <dt>

*NewID* 
</dt> <dd>

ID associato al nuovo nome dell'account di posta elettronica.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.

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

 

 




