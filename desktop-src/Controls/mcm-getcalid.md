---
title: Messaggio MCM_GETCALID (COMmctrl. h)
description: Ottiene l'ID calendario per il controllo calendario specificato. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal GETcalid.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- Controlli di Windows Message MCM_GETCALID
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb4a780d5107a7761d7dcac9b27a7cb01f3de744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120010"
---
# <a name="mcm_getcalid-message"></a>\_Messaggio MCM GETcalid

Ottiene l'ID calendario per il controllo calendario specificato. È possibile inviare questo messaggio in modo esplicito o usando la macro [**MonthCal \_ getcalid**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) .

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

ID del calendario corrente. Una delle costanti degli [identificatori del calendario](/windows/desktop/Intl/calendar-identifiers) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

