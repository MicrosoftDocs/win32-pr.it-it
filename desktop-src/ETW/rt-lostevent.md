---
description: Questa classe di tipo di evento viene usata per indicare che gli eventi sono stati persi in una sessione in tempo reale. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: RT_LostEvent classe
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
ms.openlocfilehash: d0944b843c8deb38012242111b6c5057ccf7cb8557c69caefe9a87283d2ae418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328741"
---
# <a name="rt_lostevent-class"></a>Classe RT \_ LostEvent

Questa classe di tipo di evento viene usata per indicare che gli eventi sono stati persi in una sessione in tempo reale.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a>Members

La **classe RT \_ LostEvent** non definisce membri.

## <a name="remarks"></a>Commenti

Il tipo di evento RTLostEvent indica che uno o più eventi sono stati persi. Il tipo di evento RTLostBuffer indica che uno o più buffer sono stati persi. I tipi di evento RTLostEvent e RTLostBuffer vengono recapitati prima dell'elaborazione degli eventi dal buffer.

RTLostFile indica che il file di backup usato dal logger automatico per acquisire gli eventi è stato perso.

Il disaggregamento degli eventi dipende dalla frequenza con cui vengono registrati gli eventi e dal tempo trascorso dal consumer per l'elaborazione degli eventi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento \_ perso**](lost-event.md)
</dt> </dl>

 

 




