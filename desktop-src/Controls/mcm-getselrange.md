---
title: MCM_GETSELRANGE messaggio (Commctrl.h)
description: Recupera informazioni sulla data che rappresentano i limiti superiore e inferiore dell'intervallo di date attualmente selezionato dall'utente. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro MonthCal GetSelRange.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- MCM_GETSELRANGE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- MCM_GETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7c446c98a43714a8cd839704050d2aedd1b7eab83b9199700ba24dd4e2be98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061951"
---
# <a name="mcm_getselrange-message"></a>Messaggio \_ DI MCM GETSELRANGE

Recupera informazioni sulla data che rappresentano i limiti superiore e inferiore dell'intervallo di date attualmente selezionato dall'utente. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ MonthCal GetSelRange.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice a due elementi di [**strutture SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceverà i limiti inferiore e superiore della selezione dell'utente. I limiti inferiore e superiore vengono inseriti rispettivamente in *lprgSysTimeArray* 0 e \[ \] *lprgSysTimeArray* \[ \] 1. Questo parametro deve essere un indirizzo valido e non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario. **MCM \_ GETSELRANGE avrà** esito negativo se applicato a un controllo calendario mensile che non usa lo [**stile MCS \_ MULTISELECT.**](month-calendar-control-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Ore nel controllo Calendario mensile](month-calendar-controls.md)
</dt> </dl>

 

