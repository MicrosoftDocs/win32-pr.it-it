---
title: MCM_SETMAXSELCOUNT messaggio (Commctrl.h)
description: Imposta il numero massimo di giorni che è possibile selezionare in un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro MonthCal SetMaxSelCount.
ms.assetid: 190453ab-e53b-4db7-82c1-f9d50188ad39
keywords:
- MCM_SETMAXSELCOUNT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- MCM_SETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 491e28f9af1e01a97ccbdb0d2928d35117939b82d9acc1e91ea8078aae337bcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078975"
---
# <a name="mcm_setmaxselcount-message"></a>Messaggio \_ MCM SETMAXSELCOUNT

Imposta il numero massimo di giorni che è possibile selezionare in un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ MonthCal SetMaxSelCount.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore di tipo **int** che verrà impostato per rappresentare il numero massimo di giorni che è possibile selezionare.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario. Questo messaggio avrà esito negativo se applicato a un controllo calendario mensile che non usa lo [**stile MCS \_ MULTISELECT.**](month-calendar-control-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





