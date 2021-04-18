---
title: Messaggio MCM_GETFIRSTDAYOFWEEK (COMmctrl. h)
description: Recupera il primo giorno della settimana per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetFirstDayOfWeek.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- Controlli di Windows Message MCM_GETFIRSTDAYOFWEEK
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
ms.openlocfilehash: b625e470e13c111b0274bfef422963e48c9cc7c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301940"
---
# <a name="mcm_getfirstdayofweek-message"></a>\_Messaggio GETFIRSTDAYOFWEEK MCM

Recupera il primo giorno della settimana per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **DWORD** che contiene due valori. La parola alta è un valore **bool** che è diverso da zero se il primo giorno della settimana è impostato su un valore diverso dalle impostazioni locali \_ IFIRSTDAYOFWEEK o zero in caso contrario. La parola Low è un valore INT che rappresenta il primo giorno della settimana, dove 0 è lunedì, 1 è martedì e così via.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





