---
description: Evento per utente generato da un client di messaggistica istantanea quando un utente lascia una conversazione in Controllo genitori.
ms.assetid: e6bd6bce-9eba-4192-aac8-c9e47d7180a1
title: WPCEVENT_IM_LEAVE eventi (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d814f6c9d4e3ec5acd3ee3cf3a6eb6e67d315148304f2766baf45fc633fa22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951211"
---
# <a name="wpcevent_im_leave-event"></a>Evento WPCEVENT \_ IM \_ LEAVE

Evento per utente generato da un client di messaggistica istantanea quando un utente lascia una conversazione in Controllo genitori.


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

Stringa di identità dell'account di messaggistica istantanea per questo utente.

</dd> <dt>

*ConvID* 
</dt> <dd>

Identificatore per questa conversazione.

</dd> <dt>

*LeavingIP* 
</dt> <dd>

Stringa che contiene l'indirizzo IP del computer che sta uscendo dalla conversazione.

</dd> <dt>

*LeavingUser* 
</dt> <dd>

Stringa di identità dell'account di messaggistica istantanea per l'utente che sta per uscire.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore [**dell'enumerazione WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) che indica informazioni sugli eventi che non possono essere utilizzati e sui controlli presenti.

</dd> <dt>

*MemberCount* 
</dt> <dd>

Numero di partecipanti presenti nella conversazione e con identità definite nel campo del membro.

</dd> <dt>

*Membro* 
</dt> <dd>

Stringa delimitata che contiene stringhe di identità dell'account di messaggistica istantanea per tutti i membri correnti di questa conversazione.

</dd> <dt>

*Flag* 
</dt> <dd>

Valore dell'enumerazione [**IM \_ \_ LEAVE WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_leave) che indica quando un partecipante lascia l'interazione di messaggistica istantanea.

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

 

 




