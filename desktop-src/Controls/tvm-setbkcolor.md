---
title: Messaggio TVM_SETBKCOLOR (COMmctrl. h)
description: Imposta il colore di sfondo del controllo. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetBkColor di TreeView.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- Controlli di Windows Message TVM_SETBKCOLOR
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151aef7aa61e7c66d436d0c90f2481fada017059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874010"
---
# <a name="tvm_setbkcolor-message"></a>\_Messaggio SETBKCOLOR TVM

Imposta il colore di sfondo del controllo. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetBkColor di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore di [**COLORREF**](/windows/desktop/gdi/colorref) che contiene il nuovo colore di sfondo. Se questo valore è-1, il controllo verrà ripristinato utilizzando il colore di sistema per il colore di sfondo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore di sfondo precedente. Se questo valore è-1, il controllo Usa il colore di sistema per il colore di sfondo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETBKCOLOR TVM**](tvm-getbkcolor.md)
</dt> </dl>

 

