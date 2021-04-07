---
title: Messaggio TVM_GETVISIBLECOUNT (COMmctrl. h)
description: Ottiene il numero di elementi che possono essere completamente visibili nella finestra client di un controllo di visualizzazione ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetVisibleCount di TreeView.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- Controlli di Windows Message TVM_GETVISIBLECOUNT
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1927d21741b109c5f00aa964b058dc0c34732529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963931"
---
# <a name="tvm_getvisiblecount-message"></a>\_Messaggio GETVISIBLECOUNT TVM

Ottiene il numero di elementi che possono essere completamente visibili nella finestra client di un controllo di visualizzazione ad albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetVisibleCount di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di elementi che possono essere completamente visibili nella finestra del client del controllo di visualizzazione ad albero.

## <a name="remarks"></a>Commenti

Il numero di elementi che possono essere completamente visibili può essere maggiore del numero di elementi nel controllo. Il controllo calcola questo valore dividendo l'altezza della finestra client per l'altezza di un elemento.

Si noti che il valore restituito è il numero di elementi che possono essere *completamente* visibili. Se è possibile visualizzare tutti e 20 gli elementi e parte di uno più elementi, il valore restituito è 20.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





