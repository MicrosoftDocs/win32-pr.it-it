---
title: LVM_GETGROUPSTATE messaggio (Commctrl.h)
description: Ottiene lo stato per un gruppo specificato. Inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetGroupState.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- LVM_GETGROUPSTATE di controllo Windows messaggio
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
ms.openlocfilehash: 66272dd259e80f239804ffadbd706370f948a2505173cc03aaa40057b273a629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958430"
---
# <a name="lvm_getgroupstate-message"></a>Messaggio \_ LVM GETGROUPSTATE

Ottiene lo stato per un gruppo specificato. Inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetGroupState.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Specifica il gruppo in base **a iGroupId** (vedere [**struttura LVGROUP).**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Specifica i valori di stato da recuperare. Si tratta di una combinazione dei flag elencati per **il membro di** stato di [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la combinazione di valori di stato impostati. Ad esempio, se *lParam* è LVGS COLLAPSED e il valore restituito è zero, lo stato \_ LVGS \_ COLLAPSED non è impostato. Se il gruppo non viene trovato, viene restituito zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





