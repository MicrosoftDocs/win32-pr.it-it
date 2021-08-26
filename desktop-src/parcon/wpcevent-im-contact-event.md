---
description: Evento per utente generato da un client di messaggistica istantanea quando le informazioni di contatto vengono aggiunte, modificate o rimosse in Controllo genitori.
ms.assetid: 0a016542-306e-48b4-8b0c-b9e4e915513e
title: WPCEVENT_IM_CONTACT eventi (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baac4bf5648b27f2e8d446a79bb2d90d52f0aac416e30d031d3b81d430a6927b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951449"
---
# <a name="wpcevent_im_contact-event"></a>Evento WPCEVENT \_ IM \_ CONTACT

Evento per utente generato da un client di messaggistica istantanea quando le informazioni di contatto vengono aggiunte, modificate o rimosse in Controllo genitori.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_CONTACT = {0xf, 0x0, 0x10, 0x4, 0x16, 0xf, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AppName* 
</dt> <dd>

Nome dell'applicazione di messaggistica istantanea che genera l'evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Versione dell'applicazione che genera l'evento.

</dd> <dt>

*AccountName* 
</dt> <dd>

Nome dell'account di messaggistica istantanea per questo utente.

</dd> <dt>

*Oldname* 
</dt> <dd>

Nome dell'account di messaggistica istantanea precedente, se eliminato o modificato.

</dd> <dt>

*Oldid* 
</dt> <dd>

ID associato al nome dell'account di messaggistica istantanea precedente.

</dd> <dt>

*Newname* 
</dt> <dd>

Nuovo nome dell'account di messaggistica istantanea, se aggiunto o modificato.

</dd> <dt>

*Newid* 
</dt> <dd>

ID associato al nome del nuovo account di messaggistica istantanea.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore [**dell'enumerazione WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) che indica informazioni sugli eventi che non possono essere utilizzati e sui controlli presenti.

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

 

 




