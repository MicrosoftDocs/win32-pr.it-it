---
title: LVM_GETFOCUSEDGROUP messaggio (Commctrl.h)
description: Ottiene il gruppo con lo stato attivo. Inviare questo messaggio in modo esplicito o tramite la \_ macro ListView GetFocusedGroup.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- LVM_GETFOCUSEDGROUP di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9b253405683c058518706e92e62f09041ae4db0e4bee426aa653103bda2188c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877431"
---
# <a name="lvm_getfocusedgroup-message"></a>Messaggio LVM \_ GETFOCUSEDGROUP

Ottiene il gruppo con lo stato attivo. Inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetFocusedGroup.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice del gruppo con stato LVGS FOCUSED oppure -1 se non è presente alcun gruppo con stato \_ LVGS \_ FOCUSED.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





