---
title: Messaggio MCM_SETCURSEL (COMmctrl. h)
description: Imposta la data attualmente selezionata per un controllo di calendario mensile. Se la data specificata non è visualizzata, il controllo Aggiorna la visualizzazione per visualizzarla. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- Controlli di Windows Message MCM_SETCURSEL
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
ms.openlocfilehash: cceff48fbc4ffdb7446277d506c369e1bd89c92b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302521"
---
# <a name="mcm_setcursel-message"></a>Messaggio in MCM \_

Imposta la data attualmente selezionata per un controllo di calendario mensile. Se la data specificata non è visualizzata, il controllo Aggiorna la visualizzazione per visualizzarla. È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro MonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che contiene la data da impostare come selezione corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario. Questo messaggio avrà esito negativo se applicato a un controllo calendario mensile che usa lo stile [**\_ MultiSelect MCS**](month-calendar-control-styles.md) .

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

 

