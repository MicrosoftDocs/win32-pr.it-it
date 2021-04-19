---
description: Evento per utente generato da un client di messaggistica immediata quando un utente lascia una conversazione nei controlli padre.
ms.assetid: e6bd6bce-9eba-4192-aac8-c9e47d7180a1
title: Evento WPCEVENT_IM_LEAVE (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260833a30f08330da9c622faae06f76b5d79e682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318043"
---
# <a name="wpcevent_im_leave-event"></a>\_Evento WPCEVENT im \_ Leave

Evento per utente generato da un client di messaggistica immediata quando un utente lascia una conversazione nei controlli padre.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_LEAVE = {0x9, 0x0, 0x10, 0x4, 0x16, 0x9, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AppName* 
</dt> <dd>

Nome dell'applicazione che genera l'evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Stringa di versione per l'applicazione che genera l'evento.

</dd> <dt>

*AccountName* 
</dt> <dd>

Stringa di identità dell'account di messaggistica immediata per questo utente.

</dd> <dt>

*ConvID* 
</dt> <dd>

Identificatore di questa conversazione.

</dd> <dt>

*LeavingIP* 
</dt> <dd>

Stringa che contiene l'indirizzo IP del computer che sta lasciando questa conversazione.

</dd> <dt>

*LeavingUser* 
</dt> <dd>

Stringa di identità dell'account di messaggistica immediata per l'utente che sta lasciando.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.

</dd> <dt>

*MemberCount* 
</dt> <dd>

Il numero di partecipanti che si trovano nella conversazione e con le identità definite nel campo del membro.

</dd> <dt>

*Membro* 
</dt> <dd>

Stringa delimitata che contiene le stringhe di identità dell'account di messaggistica immediata per tutti i membri correnti di questa conversazione.

</dd> <dt>

*Flag* 
</dt> <dd>

Valore dell'enumerazione [**WPCFLAG \_ im \_ Leave**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_leave) che indica le informazioni relative al momento in cui un partecipante lascia l'interazione di messaggistica immediata.

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

 

 




