---
description: Evento a livello di sistema generato dai criteri di restrizione software quando un'applicazione è bloccata da regole più sicure.
ms.assetid: 6772a2c9-35c1-4b75-94e4-baa84af7c0ed
title: WPCEVENT_SYSTEM_APPBLOCKED eventi (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0444cee0a2844ae868923b5cf51923e0024c9de9a2a12ad51e20d8db9fa3b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112721"
---
# <a name="wpcevent_system_appblocked-event"></a>Evento WPCEVENT \_ SYSTEM \_ APPBLOCKED

Evento a livello di sistema generato dai criteri di restrizione software quando un'applicazione è bloccata da regole più sicure.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYSTEM_APPBLOCKED = {0x10, 0x0, 0x10, 0x4, 0x16, 0x10, 0x8000000000000010};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Timestamp* 
</dt> <dd>

Ora in cui si è verificato il blocco.

</dd> <dt>

*UserID* 
</dt> <dd>

Identificatore di sicurezza dell'utente che sta tentando di avviare l'applicazione.

</dd> <dt>

*Percorso* 
</dt> <dd>

Percorso dell'applicazione che l'utente sta tentando di avviare.

</dd> <dt>

*RuleID* 
</dt> <dd>

ID della regola all'interno del set di regole più sicure di Controllo genitori che blocca l'esecuzione.

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

 

 




