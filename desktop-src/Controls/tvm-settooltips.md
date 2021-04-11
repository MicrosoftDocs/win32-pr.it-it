---
title: Messaggio TVM_SETTOOLTIPS (COMmctrl. h)
description: Imposta il controllo ToolTip figlio di un controllo di visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TreeView Setooltips.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- Controlli di Windows Message TVM_SETTOOLTIPS
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd9d5957a38d873993405a5283545472433e958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119730"
---
# <a name="tvm_settooltips-message"></a>\_Messaggio di SEtooltips TVM

Imposta il controllo ToolTip figlio di un controllo di visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**TreeView \_ setooltips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per un controllo ToolTip.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo ToolTip impostato in precedenza per il controllo di visualizzazione ad albero oppure **null** se le descrizioni comandi non sono state usate in precedenza.

## <a name="remarks"></a>Commenti

Quando vengono creati, i controlli di visualizzazione albero creano automaticamente un controllo ToolTip figlio. Per impedire a un controllo di visualizzazione albero di usare le descrizioni comandi, creare il controllo con lo stile [**\_ notooltips di TV**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_descrizioni comando TVM**](tvm-gettooltips.md)
</dt> </dl>

 

 





