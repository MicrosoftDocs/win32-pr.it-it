---
title: Messaggio MCM_GETTODAY (COMmctrl. h)
description: Recupera le informazioni sulla data per la data specificata come \ 0034; Today \ 0034; per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal GetToday.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- Controlli di Windows Message MCM_GETTODAY
topic_type:
- apiref
api_name:
- MCM_GETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21538af3c573b3d972b7f16bfe024e0d36211644
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964291"
---
# <a name="mcm_gettoday-message"></a>\_Messaggio MCM GETtoday

Recupera le informazioni sulla data per la data specificata come "Today" per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la macro [**MonthCal \_ GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceverà le informazioni sulla data. Questo parametro deve essere un indirizzo valido e non può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

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

 

