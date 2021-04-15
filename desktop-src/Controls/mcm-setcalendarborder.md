---
title: Messaggio MCM_SETCALENDARBORDER (COMmctrl. h)
description: Imposta la dimensione, in pixel, del bordo. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal SetCalendarBorder.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- Controlli di Windows Message MCM_SETCALENDARBORDER
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
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476625"
---
# <a name="mcm_setcalendarborder-message"></a>\_Messaggio SETCALENDARBORDER MCM

Imposta la dimensione, in pixel, del bordo. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Se **true**, la dimensione del bordo è impostata sul numero di pixel specificato da *lParam* . Se **false**, le dimensioni del bordo vengono reimpostate sul valore predefinito specificato dal tema oppure su zero se i temi non vengono usati.

</dd> <dt>

*lParam* 
</dt> <dd>

Numero di pixel della dimensione del bordo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non usato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





