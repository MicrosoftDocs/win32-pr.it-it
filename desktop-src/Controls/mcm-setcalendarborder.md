---
title: MCM_SETCALENDARBORDER messaggio (Commctrl.h)
description: Imposta le dimensioni del bordo, in pixel. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal SetCalendarBorder.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- MCM_SETCALENDARBORDER controlli Windows messaggio
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e020ad282ce21555e6c3a74198a0034013ac1d7cfac8f4eb68e52137e5f684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697201"
---
# <a name="mcm_setcalendarborder-message"></a>MESSAGGIO \_ DI MCM SETCALENDARBORDER

Imposta le dimensioni del bordo, in pixel. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ MonthCal SetCalendarBorder.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Se **TRUE,** le dimensioni del bordo vengono impostate sul numero di pixel specificato *da lParam.* Se **FALSE,** le dimensioni del bordo vengono reimpostate sul valore predefinito specificato dal tema oppure su zero se i temi non vengono usati.

</dd> <dt>

*lParam* 
</dt> <dd>

Numero di pixel delle dimensioni del bordo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non usato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





