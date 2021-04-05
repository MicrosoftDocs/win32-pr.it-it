---
title: Messaggio TVM_GETEXTENDEDSTYLE (COMmctrl. h)
description: Recupera lo stile esteso per un controllo di visualizzazione albero. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetExtendedStyle di TreeView.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- Controlli di Windows Message TVM_GETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a00e125389ff56c7ff93370ab71945598dba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874481"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a>Messaggio TVM_GETEXTENDEDSTYLE (COMmctrl. h)

Recupera lo stile esteso per un controllo di visualizzazione albero. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetExtendedStyle di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore dello stile esteso. Per altre informazioni sugli stili, vedere [stili estesi del controllo di visualizzazione albero](tree-view-control-window-extended-styles.md).

## <a name="remarks"></a>Commenti

Gli stili estesi per un controllo di visualizzazione albero non hanno nulla a che fare con gli stili estesi usati con la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

