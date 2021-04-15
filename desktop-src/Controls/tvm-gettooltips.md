---
title: Messaggio TVM_GETTOOLTIPS (COMmctrl. h)
description: Recupera l'handle per il controllo ToolTip figlio utilizzato da un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TreeView GetToolTips.
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- Controlli di Windows Message TVM_GETTOOLTIPS
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475898"
---
# <a name="tvm_gettooltips-message"></a>\_Messaggio TVM GETtooltips

Recupera l'handle per il controllo ToolTip figlio utilizzato da un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TreeView \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo ToolTip figlio oppure **null** se il controllo non utilizza descrizioni comandi.

## <a name="remarks"></a>Commenti

Quando vengono creati, i controlli di visualizzazione albero creano automaticamente un controllo ToolTip figlio. Per fare in modo che un controllo di visualizzazione albero non usi descrizioni comandi, creare il controllo con lo stile [**\_ notooltips di TV**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_descrizioni comando TVM**](tvm-settooltips.md)
</dt> </dl>

 

 





