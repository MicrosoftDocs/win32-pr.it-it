---
description: Evento per utente generato dal filtro contenuto Web a causa del tentativo di accedere a un URL.
ms.assetid: 636b0ce8-cf08-4536-9b41-79512b02a066
title: WPCEVENT_WEB_URLVISIT evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9524909ee78d14395e2f208fe265b3abc31240d2036788b8b84c4fea05aac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112701"
---
# <a name="wpcevent_web_urlvisit-event"></a>Evento WPCEVENT \_ WEB \_ URLVISIT

Evento per utente generato dal filtro contenuto Web a causa del tentativo di accedere a un URL.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_URLVISIT = {0x3, 0x0, 0x10, 0x4, 0x18, 0x3, 0x8000000000000010};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*URL* 
</dt> <dd>

URL che sta tentando di essere aperto.

</dd> <dt>

*Applicazione* 
</dt> <dd>

Applicazione che genera l'evento.

</dd> <dt>

*Version* 
</dt> <dd>

Stringa di versione per l'applicazione.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valore [**dell'enumerazione WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) che indica quali eventi non possono essere utilizzati e quali controlli sono presenti.

</dd> <dt>

*RatingSystemID* 
</dt> <dd>

GUID che identifica il sistema di classificazione corrente.

</dd> <dt>

*CatCount* 
</dt> <dd>

Numero di voci bloccate nel campo della categoria.

</dd> <dt>

*Categoria* 
</dt> <dd>

Stringa delimitata di identificatori di categoria bloccati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso delle API di registrazione per Controllo genitori](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




