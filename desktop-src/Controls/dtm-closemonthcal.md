---
title: DTM_CLOSEMONTHCAL messaggio (Commctrl.h)
description: Chiude un controllo selezione data e ora (DTP). Inviare questo messaggio in modo esplicito o usando la \_ macro DateTime CloseMonthCal.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- DTM_CLOSEMONTHCAL dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f458592d2842625b9826eda5963c66cbd182e3f052a2b2a70ff5219a054e8cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878241"
---
# <a name="dtm_closemonthcal-message"></a>Messaggio DTM \_ CLOSEMONTHCAL

Chiude un controllo selezione data e ora (DTP). Inviare questo messaggio in modo esplicito o usando la macro [**\_ DateTime CloseMonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero.

## <a name="remarks"></a>Commenti

Elimina il controllo e invia una notifica [DTN \_ CLOSEUP](dtn-closeup.md) che indica che il controllo è in chiusura anziché il controllo è in corso di apertura (elenco a discesa come nella notifica [DTN \_ DROPDOWN)](dtn-dropdown.md) all'elemento padre del controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[ELENCO A DISCESA DTN \_](dtn-dropdown.md)
</dt> <dt>

[CHIUSURA \_ DTN](dtn-closeup.md)
</dt> </dl>

 

 





