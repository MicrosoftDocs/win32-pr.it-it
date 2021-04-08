---
description: Evento per utente generato dal filtro contenuto Web a causa del tentativo di accedere a un URL.
ms.assetid: 636b0ce8-cf08-4536-9b41-79512b02a066
title: Evento WPCEVENT_WEB_URLVISIT (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1075ae930cdaa9ee539dbc17a8c13d5c2a41add
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049972"
---
# <a name="wpcevent_web_urlvisit-event"></a>\_ \_ Evento URLVISIT Web WPCEVENT

Evento per utente generato dal filtro contenuto Web a causa del tentativo di accedere a un URL.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_URLVISIT = {0x3, 0x0, 0x10, 0x4, 0x18, 0x3, 0x8000000000000010};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*URL* 
</dt> <dd>

URL che sta tentando di aprire.

</dd> <dt>

*Applicazione* 
</dt> <dd>

Applicazione che genera l'evento.

</dd> <dt>

*Versione* 
</dt> <dd>

Stringa di versione per l'applicazione.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.

</dd> <dt>

*RatingSystemID* 
</dt> <dd>

GUID che identifica il sistema di classificazione corrente.

</dd> <dt>

*CatCount* 
</dt> <dd>

Numero di voci bloccate nel campo categoria.

</dd> <dt>

*Categoria* 
</dt> <dd>

Stringa delimitata di identificatori di categoria bloccati.

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

 

 




