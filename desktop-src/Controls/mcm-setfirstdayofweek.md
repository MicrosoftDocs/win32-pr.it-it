---
title: Messaggio MCM_SETFIRSTDAYOFWEEK (COMmctrl. h)
description: Imposta il primo giorno della settimana per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal setFirstDayOfWeek.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- Controlli di Windows Message MCM_SETFIRSTDAYOFWEEK
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
ms.openlocfilehash: a32452c9043bbd7c3bbcf96f9dc32e67714eacce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302519"
---
# <a name="mcm_setfirstdayofweek-message"></a>\_Messaggio SETFIRSTDAYOFWEEK MCM

Imposta il primo giorno della settimana per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ setFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore di tipo **int** che rappresenta il giorno da impostare come primo giorno della settimana, dove 0 è lunedì, 1 è martedì e così via.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **DWORD** che contiene due valori. La parola alta è un valore **bool** che è diverso da zero se il primo giorno della settimana precedente non era uguale a IFIRSTDAYOFWEEK delle impostazioni locali \_ , altrimenti zero. La parola Low è un valore INT che rappresenta il primo giorno della settimana precedente.

## <a name="remarks"></a>Commenti

Se il primo giorno della settimana è impostato su un valore diverso da quello predefinito (impostazioni locali \_ IFIRSTDAYOFWEEK), il controllo non aggiornerà automaticamente le modifiche del primo giorno della settimana in base alle modifiche delle impostazioni locali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





