---
title: MCM_SETCALID messaggio (Commctrl.h)
description: Imposta l'ID calendario per il controllo calendario specificato. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro MonthCal SetCALID.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- MCM_SETCALID controlli di Windows messaggio
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
ms.openlocfilehash: b40e7f4577382aa0e003165e38e4557b8dc234592f747a579e5a071ce2440a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575581"
---
# <a name="mcm_setcalid-message"></a>Messaggio \_ MCM SETCALID

Imposta l'ID calendario per il controllo calendario specificato. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ MonthCal SetCALID.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

ID del calendario. Una delle [costanti Calendar Identifiers.](/windows/desktop/Intl/calendar-identifiers)

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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

