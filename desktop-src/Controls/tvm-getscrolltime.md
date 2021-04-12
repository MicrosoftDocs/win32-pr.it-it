---
title: Messaggio TVM_GETSCROLLTIME (COMmctrl. h)
description: Recupera il tempo massimo di scorrimento per il controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetScrollTime di TreeView.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- Controlli di Windows Message TVM_GETSCROLLTIME
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f0bacc6c12dd7f54f20d882faf738c11848d59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119315"
---
# <a name="tvm_getscrolltime-message"></a>\_Messaggio GETSCROLLTIME TVM

Recupera il tempo massimo di scorrimento per il controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetScrollTime di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il tempo massimo di scorrimento, in millisecondi.

## <a name="remarks"></a>Commenti

Il tempo massimo di scorrimento è la quantità di tempo più lungo che può essere eseguita da un'operazione di scorrimento. Lo scorrimento verrà regolato in modo che lo scorrimento avvenga entro il tempo massimo di scorrimento. Un'operazione di scorrimento potrebbe richiedere meno tempo rispetto al valore massimo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETSCROLLTIME TVM**](tvm-setscrolltime.md)
</dt> </dl>

 

 





