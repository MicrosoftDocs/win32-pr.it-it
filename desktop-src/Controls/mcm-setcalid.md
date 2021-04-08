---
title: Messaggio MCM_SETCALID (COMmctrl. h)
description: Imposta l'ID calendario per il controllo calendario specificato. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- Controlli di Windows Message MCM_SETCALID
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a661a685062fe737a1927c3a6ab455e8499c6ca9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047997"
---
# <a name="mcm_setcalid-message"></a>Messaggio in MCM \_

Imposta l'ID calendario per il controllo calendario specificato. È possibile inviare questo messaggio in modo esplicito o usando [**la \_ macro MonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

ID del calendario. Una delle costanti degli [identificatori del calendario](/windows/desktop/Intl/calendar-identifiers) .

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

