---
description: Evento per utente generato da un'applicazione di messaggistica immediata quando un'entità tenta di partecipare a una conversazione in corso nei controlli padre.
ms.assetid: 5251234b-0280-4d5d-80f5-295d720a89d1
title: Evento WPCEVENT_IM_JOIN (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b020eb3d4204f946002f59f472e5c95b715f88f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881413"
---
# <a name="wpcevent_im_join-event"></a>\_Evento WPCEVENT im \_ join

Evento per utente generato da un'applicazione di messaggistica immediata quando un'entità tenta di partecipare a una conversazione in corso nei controlli padre.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_JOIN = {0x8, 0x0, 0x10, 0x4, 0x16, 0x8, 0x8000000000000030};
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

*JoiningIP* 
</dt> <dd>

Stringa che contiene l'indirizzo IP del computer che partecipa a questa conversazione.

</dd> <dt>

*JoiningUser* 
</dt> <dd>

Stringa di identità dell'account di messaggistica immediata per l'utente che partecipa.

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

*Mittente* 
</dt> <dd>

Stringa di identità dell'account di messaggistica immediata per l'utente che sta effettuando la richiesta per partecipare alla conversazione.

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

 

 




