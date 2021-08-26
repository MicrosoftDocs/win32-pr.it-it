---
title: MCM_SETCURSEL messaggio (Commctrl.h)
description: Imposta la data attualmente selezionata per un controllo calendario mensile. Se la data specificata non è visualizzata, il controllo aggiorna la visualizzazione per visualizzarla. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro MonthCal SetCurSel.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- MCM_SETCURSEL di controllo Windows messaggio
topic_type:
- apiref
api_name:
- MCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63238f11f93e56c18e1897fcdd3cb96977f23fe16bde19123b5c063f99c0ff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061891"
---
# <a name="mcm_setcursel-message"></a>Messaggio \_ DI MCM SETCURSEL

Imposta la data attualmente selezionata per un controllo calendario mensile. Se la data specificata non è visualizzata, il controllo aggiorna la visualizzazione per visualizzarla. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ MonthCal SetCurSel.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contenente la data da impostare come selezione corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario. Questo messaggio avrà esito negativo se applicato a un controllo calendario mensile che usa lo [**stile MCS \_ MULTISELECT.**](month-calendar-control-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Ore nel controllo Calendario mensile](month-calendar-controls.md)
</dt> </dl>

 

