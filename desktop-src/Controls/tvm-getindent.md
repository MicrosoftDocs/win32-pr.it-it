---
title: Messaggio TVM_GETINDENT (COMmctrl. h)
description: Recupera la quantità, in pixel, in base alla quale gli elementi figlio vengono rientrati rispetto ai relativi elementi padre. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TreeView GetIndent.
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- Controlli di Windows Message TVM_GETINDENT
topic_type:
- apiref
api_name:
- TVM_GETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33775341adc47d84ead9a633d7d31b16ffc4a723
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874478"
---
# <a name="tvm_getindent-message"></a>\_Messaggio TVM GETindent

Recupera la quantità, in pixel, in base alla quale gli elementi figlio vengono rientrati rispetto ai relativi elementi padre. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TreeView \_ GetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la quantità di rientri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





