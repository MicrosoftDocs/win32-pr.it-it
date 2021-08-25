---
title: DTM_SETMCSTYLE messaggio (Commctrl.h)
description: Imposta lo stile di un controllo selezione data e ora (DTP). Inviare questo messaggio in modo esplicito o usando la \_ macro DateTime SetMonthCalStyle.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- DTM_SETMCSTYLE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2805f2213bcbb1fa91a10ea80005b8b23bbc7447973bba6930bfdcb1e52a9e91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877801"
---
# <a name="dtm_setmcstyle-message"></a>Messaggio DTM \_ SETMCSTYLE

Imposta lo stile di un controllo selezione data e ora (DTP). Inviare questo messaggio in modo esplicito o usando la macro [**\_ DateTime SetMonthCalStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>Valore di stile. Per altre informazioni, vedere <a href="month-calendar-control-styles.md">Month Calendar Control Styles</a>.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore dello stile precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





