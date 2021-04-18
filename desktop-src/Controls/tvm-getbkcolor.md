---
title: Messaggio TVM_GETBKCOLOR (COMmctrl. h)
description: Recupera il colore di sfondo corrente del controllo. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetBkColor di TreeView.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- Controlli di Windows Message TVM_GETBKCOLOR
topic_type:
- apiref
api_name:
- TVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8077bc9655c088aceefe239ed019cc45874d38ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302279"
---
# <a name="tvm_getbkcolor-message"></a>\_Messaggio GETBKCOLOR TVM

Recupera il colore di sfondo corrente del controllo. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetBkColor di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore di sfondo corrente. Se questo valore è-1, il controllo Usa il colore di sistema per il colore di sfondo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETBKCOLOR TVM**](tvm-setbkcolor.md)
</dt> </dl>

 

