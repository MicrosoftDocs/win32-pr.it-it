---
description: Questa classe di tipo evento viene utilizzata per indicare che gli eventi sono stati persi in una sessione in tempo reale. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: Classe RT_LostEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RT_LostEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: b689dd95aa1e078572d33de64f245e4844698d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526383"
---
# <a name="rt_lostevent-class"></a>RT \_ LostEvent (classe)

Questa classe di tipo evento viene utilizzata per indicare che gli eventi sono stati persi in una sessione in tempo reale.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a>Members

La classe **RT \_ LostEvent** non definisce membri.

## <a name="remarks"></a>Commenti

Il tipo di evento RTLostEvent indica che uno o più eventi sono stati persi. Il tipo di evento RTLostBuffer indica che uno o più buffer sono stati persi. I tipi di evento RTLostEvent e RTLostBuffer vengono recapitati prima di elaborare gli eventi dal buffer.

RTLostFile indica che il file di supporto usato dall'autologger per acquisire gli eventi è andato perso.

La perdita di eventi dipende dalla frequenza con cui gli eventi vengono registrati e dal tempo impiegato dall'utente per l'elaborazione degli eventi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Evento perso**](lost-event.md)
</dt> </dl>

 

 




