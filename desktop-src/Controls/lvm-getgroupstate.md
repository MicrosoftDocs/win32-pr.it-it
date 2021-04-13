---
title: Messaggio LVM_GETGROUPSTATE (COMmctrl. h)
description: Ottiene lo stato di un gruppo specificato. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetGroupState di ListView.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- Controlli di Windows Message LVM_GETGROUPSTATE
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475376"
---
# <a name="lvm_getgroupstate-message"></a>\_Messaggio GETGROUPSTATE LVM

Ottiene lo stato di un gruppo specificato. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetGroupState di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Specifica il gruppo per **iGroupId** (vedere la struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Specifica i valori di stato da recuperare. Si tratta di una combinazione dei flag elencati per il membro di **stato** di [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la combinazione di valori di stato impostati. Se, ad esempio, *lParam* è LVGS \_ compresso e il valore restituito è zero, lo \_ stato compresso LVGS non è impostato. Se il gruppo non viene trovato, viene restituito zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





