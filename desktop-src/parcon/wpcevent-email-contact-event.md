---
description: Evento per utente generato da un client di posta elettronica che registra quando un contatto viene aggiunto, modificato o eliminato in Controllo genitori.
ms.assetid: 9d1f52ef-ff49-4c0d-a48a-93aeccbe7f2b
title: WPCEVENT_EMAIL_CONTACT eventi (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d84a450c53705dae2db777081f7177f43505e0481ae38a67c1b90e507fa4a5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951571"
---
# <a name="wpcevent_email_contact-event"></a>Evento CONTACT \_ WPCEVENT EMAIL \_

Evento per utente generato da un client di posta elettronica che registra quando un contatto viene aggiunto, modificato o eliminato in Controllo genitori.


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

*Oldname* 
</dt> <dd>

Nome dell'account di posta elettronica precedente, se eliminato o modificato.

</dd> <dt>

*Oldid* 
</dt> <dd>

ID associato al nome dell'account di posta elettronica precedente.

</dd> <dt>

*Newname* 
</dt> <dd>

Nome del nuovo account di posta elettronica, se aggiunto o modificato.

</dd> <dt>

*Newid* 
</dt> <dd>

ID associato al nome del nuovo account di posta elettronica.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore [**dell'enumerazione WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) che indica informazioni sugli eventi che non possono essere utilizzati e sui controlli presenti.

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

 

 




