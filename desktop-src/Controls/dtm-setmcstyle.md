---
title: Messaggio DTM_SETMCSTYLE (COMmctrl. h)
description: Imposta lo stile di un controllo di selezione data e ora (DTP). Inviare questo messaggio in modo esplicito o utilizzando la \_ macro DateTime SetMonthCalStyle.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- Controlli di Windows Message DTM_SETMCSTYLE
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
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120543"
---
# <a name="dtm_setmcstyle-message"></a>\_Messaggio SETMCSTYLE DTM

Imposta lo stile di un controllo di selezione data e ora (DTP). Inviare questo messaggio in modo esplicito o utilizzando la macro [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>Valore di stile. Per altre informazioni, vedere <a href="month-calendar-control-styles.md">stili del controllo calendario mensile</a>.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore dello stile precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





