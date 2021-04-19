---
description: Evento a livello di sistema generato da criteri di restrizione software quando un'applicazione viene bloccata da regole più sicure.
ms.assetid: 6772a2c9-35c1-4b75-94e4-baa84af7c0ed
title: Evento WPCEVENT_SYSTEM_APPBLOCKED (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c3f6255911f59717c1fa594aee4bfc49f6c5a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311575"
---
# <a name="wpcevent_system_appblocked-event"></a>\_Evento APPBLOCKED di sistema WPCEVENT \_

Evento a livello di sistema generato da criteri di restrizione software quando un'applicazione viene bloccata da regole più sicure.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYSTEM_APPBLOCKED = {0x10, 0x0, 0x10, 0x4, 0x16, 0x10, 0x8000000000000010};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TimeStamp* 
</dt> <dd>

Data e ora in cui si è verificato il blocco.

</dd> <dt>

*UserID* 
</dt> <dd>

ID di sicurezza dell'utente che sta tentando di avviare l'applicazione.

</dd> <dt>

*Percorso* 
</dt> <dd>

Percorso dell'applicazione che l'utente sta tentando di avviare.

</dd> <dt>

*RuleID* 
</dt> <dd>

ID della regola nel set di controlli padre regole più sicure che sta bloccando l'esecuzione.

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

 

 




