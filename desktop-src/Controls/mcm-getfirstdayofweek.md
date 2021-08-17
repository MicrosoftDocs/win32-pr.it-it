---
title: MCM_GETFIRSTDAYOFWEEK messaggio (Commctrl.h)
description: Recupera il primo giorno della settimana per un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la macro MonthCal \_ GetFirstDayOfWeek.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- MCM_GETFIRSTDAYOFWEEK controlli Windows messaggio
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc0ddcd36da0b993f3a05092c878319a6749d9eb5a3043ce910eba1462beef9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319651"
---
# <a name="mcm_getfirstdayofweek-message"></a>Messaggio \_ MCM GETFIRSTDAYOFWEEK

Recupera il primo giorno della settimana per un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la macro [**MonthCal \_ GetFirstDayOfWeek.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che contiene due valori. La parola alta è un **valore BOOL** diverso da zero se il primo giorno della settimana è impostato su un valore diverso da LOCALE \_ IFIRSTDAYOFWEEK o zero in caso contrario. La parola bassa è un valore INT che rappresenta il primo giorno della settimana, dove 0 è lunedì, 1 è martedì e così via.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





