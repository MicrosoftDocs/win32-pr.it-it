---
description: Evento per utente generato da un client di messaggistica immediata quando le funzionalità definite vengono usate nei controlli padre.
ms.assetid: 45e80314-90b1-4fcf-9c8f-c9840ae1775b
title: Evento WPCEVENT_IM_FEATURE (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee28f004560ed287bc3cb94cbee1bda876355834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967380"
---
# <a name="wpcevent_im_feature-event"></a>\_ \_ Evento funzionalità im WPCEVENT

Evento per utente generato da un client di messaggistica immediata quando le funzionalità definite vengono usate nei controlli padre.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_FEATURE = {0xb, 0x0, 0x10, 0x4, 0x16, 0xb, 0x8000000000000030};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AppName* 
</dt> <dd>

Nome dell'applicazione di messaggistica immediata.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Stringa di versione per l'applicazione.

</dd> <dt>

*AccountName* 
</dt> <dd>

Nome dell'account di messaggistica immediata di questo utente.

</dd> <dt>

*ConvID* 
</dt> <dd>

ID della conversazione.

</dd> <dt>

*MediaType* 
</dt> <dd>

Valore dell'enumerazione della [**\_ \_ funzionalità WPCFLAG im**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_feature) che indica informazioni sulle funzionalità a cui si accede durante un'interazione di messaggistica immediata.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Il numero di utenti di messaggistica immediata che ricevono la funzionalità e che hanno identità definite nel campo del destinatario.

</dd> <dt>

*Recipient* 
</dt> <dd>

Stringa delimitata che contiene le identità di account di messaggistica immediata di tutti gli utenti che ricevono la funzionalità.

</dd> <dt>

*Mittente* 
</dt> <dd>

Nome dell'account di messaggistica immediata per l'utente che ha origine la funzionalità.

</dd> <dt>

*SenderIP* 
</dt> <dd>

Indirizzo IP del computer del mittente.

</dd> <dt>

*Dati* 
</dt> <dd>

Descrizione dei dati della funzionalità.

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

 

 




