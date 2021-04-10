---
title: Messaggio TVM_SETINSERTMARKCOLOR (COMmctrl. h)
description: Imposta il colore utilizzato per creare il segno di inserimento per la visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetInsertMarkColor di TreeView.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- Controlli di Windows Message TVM_SETINSERTMARKCOLOR
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92668b1137b089f9a09cc9a34d63d472742bce4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120102"
---
# <a name="tvm_setinsertmarkcolor-message"></a>\_Messaggio SETINSERTMARKCOLOR TVM

Imposta il colore utilizzato per creare il segno di inserimento per la visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetInsertMarkColor di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore di [**COLORREF**](/windows/desktop/gdi/colorref) che contiene il nuovo colore del segno di inserimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **COLORREF** che contiene il colore del segno di inserimento precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETINSERTMARKCOLOR TVM**](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

