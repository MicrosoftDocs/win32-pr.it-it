---
title: Messaggio LVM_GETFOCUSEDGROUP (COMmctrl. h)
description: Ottiene il gruppo con lo stato attivo. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetFocusedGroup di ListView.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- Controlli di Windows Message LVM_GETFOCUSEDGROUP
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
ms.openlocfilehash: 3e0d12eb637ec1a421a5eaff58636df7bef8f449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475166"
---
# <a name="lvm_getfocusedgroup-message"></a>\_Messaggio GETFOCUSEDGROUP LVM

Ottiene il gruppo con lo stato attivo. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetFocusedGroup di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice del gruppo con stato LVGS \_ attivo oppure-1 se non è presente alcun gruppo con lo stato LVGS \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





