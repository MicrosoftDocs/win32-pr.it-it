---
title: MCM_SETFIRSTDAYOFWEEK messaggio (Commctrl.h)
description: Imposta il primo giorno della settimana per un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la macro MonthCal \_ SetFirstDayOfWeek.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- MCM_SETFIRSTDAYOFWEEK dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- MCM_SETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e34732257c18acceec3fd7db9807753e9a930e106198b33a0dd61dc27a33eef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077111"
---
# <a name="mcm_setfirstdayofweek-message"></a>Messaggio \_ MCM SETFIRSTDAYOFWEEK

Imposta il primo giorno della settimana per un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MonthCal \_ SetFirstDayOfWeek.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore di tipo **int** che rappresenta il giorno da impostare come primo giorno della settimana, dove 0 è lunedì, 1 è martedì e così via.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che contiene due valori. La parola alta è un **valore BOOL** diverso da zero se il primo giorno della settimana precedente non è uguale a LOCALE \_ IFIRSTDAYOFWEEK o zero in caso contrario. La parola bassa è un valore INT che rappresenta il primo giorno della settimana precedente.

## <a name="remarks"></a>Commenti

Se il primo giorno della settimana è impostato su un valore diverso da quello predefinito (LOCALE IFIRSTDAYOFWEEK), il controllo non aggiornerà automaticamente le modifiche del primo giorno della settimana in base alle modifiche delle impostazioni \_ locali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





