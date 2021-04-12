---
description: Evento per utente generato da un client di messaggistica immediata quando le informazioni di contatto vengono aggiunte, modificate o rimosse nei controlli padre.
ms.assetid: 0a016542-306e-48b4-8b0c-b9e4e915513e
title: Evento WPCEVENT_IM_CONTACT (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9747f7ede57f7a1d77af0f0e8e5425401ee32b36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233733"
---
# <a name="wpcevent_im_contact-event"></a>\_ \_ Evento contatto WPCEVENT im

Evento per utente generato da un client di messaggistica immediata quando le informazioni di contatto vengono aggiunte, modificate o rimosse nei controlli padre.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_CONTACT = {0xf, 0x0, 0x10, 0x4, 0x16, 0xf, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AppName* 
</dt> <dd>

Nome dell'applicazione di messaggistica immediata che genera l'evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Versione dell'applicazione che genera l'evento.

</dd> <dt>

*AccountName* 
</dt> <dd>

Nome dell'account di messaggistica immediata per questo utente.

</dd> <dt>

*OldName* 
</dt> <dd>

Nome dell'account di messaggistica istantanea precedente, se eliminato o modificato.

</dd> <dt>

*OldID* 
</dt> <dd>

ID associato al nome dell'account di messaggistica immediata precedente.

</dd> <dt>

*NewName* 
</dt> <dd>

Il nuovo nome dell'account di messaggistica immediata, se aggiunto o modificato.

</dd> <dt>

*NewID* 
</dt> <dd>

ID associato al nuovo nome dell'account di messaggistica immediata.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.

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

 

 




