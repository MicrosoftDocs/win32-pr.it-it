---
title: Messaggio MCM_GETSELRANGE (COMmctrl. h)
description: Recupera le informazioni sulla data che rappresentano i limiti superiore e inferiore dell'intervallo di date attualmente selezionato dall'utente. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetSelRange.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- Controlli di Windows Message MCM_GETSELRANGE
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
ms.openlocfilehash: b0d2f922b013a3eab525228bda4f5b99f33e70d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964043"
---
# <a name="mcm_getselrange-message"></a>\_Messaggio GETSELRANGE MCM

Recupera le informazioni sulla data che rappresentano i limiti superiore e inferiore dell'intervallo di date attualmente selezionato dall'utente. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice a due elementi di strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceverà i limiti inferiore e superiore della selezione dell'utente. I limiti inferiore e superiore vengono inseriti rispettivamente in *lprgSysTimeArray* \[ 0 \] e *lprgSysTimeArray* \[ 1 \] . Questo parametro deve essere un indirizzo valido e non può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario. **MCM \_ GETSELRANGE** avrà esito negativo se applicato a un controllo calendario mensile che non usa lo stile [**\_ MultiSelect MCS**](month-calendar-control-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Orari del controllo calendario mensile](month-calendar-controls.md)
</dt> </dl>

 

