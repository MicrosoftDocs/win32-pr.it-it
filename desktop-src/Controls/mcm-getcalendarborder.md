---
title: Messaggio MCM_GETCALENDARBORDER (COMmctrl. h)
description: Ottiene la dimensione, in pixel, del bordo. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetCurrentView.
ms.assetid: 68366ee1-7511-46a5-aab0-a42fb80c265f
keywords:
- Controlli di Windows Message MCM_GETCALENDARBORDER
topic_type:
- apiref
api_name:
- MCM_GETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581eeb5c060f725d3f884f4c19d7d3da3023c63a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518292"
---
# <a name="mcm_getcalendarborder-message"></a>\_Messaggio GETCALENDARBORDER MCM

Ottiene la dimensione, in pixel, del bordo. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dimensioni del bordo, in pixel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





