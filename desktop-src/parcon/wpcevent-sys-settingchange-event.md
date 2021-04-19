---
description: Evento a livello di sistema generato da un'impostazione di controlli padre.
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: Evento WPCEVENT_SYS_SETTINGCHANGE (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0efb4d68fabcb5f9216c4ccf3bb923ee0ff54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318042"
---
# <a name="wpcevent_sys_settingchange-event"></a>\_Evento WPCEVENT sys \_ SETTINGCHANGE

Evento a livello di sistema generato da un'impostazione di controlli padre.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Classe* 
</dt> <dd>

Classe che genera l'evento.

</dd> <dt>

*Impostazione* 
</dt> <dd>

Valore dell'enumerazione di **\_ Impostazioni WPC** .

</dd> <dt>

*Proprietario* 
</dt> <dd>

Identificatore di sicurezza dell'utente che genera l'evento.

</dd> <dt>

*OldVal* 
</dt> <dd>

Valore precedente di questa impostazione, se eliminato o modificato.

</dd> <dt>

*NewVal* 
</dt> <dd>

Nuovo valore di questa impostazione, se aggiunto o modificato.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.

</dd> <dt>

*Facoltativo* 
</dt> <dd>

Campo facoltativo.

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

 

 




