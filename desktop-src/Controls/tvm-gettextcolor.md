---
title: Messaggio TVM_GETTEXTCOLOR (COMmctrl. h)
description: Recupera il colore del testo corrente del controllo. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetTextColor di TreeView.
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- Controlli di Windows Message TVM_GETTEXTCOLOR
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899fc68847fea937a6f62bff6367eeac5570a5a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048107"
---
# <a name="tvm_gettextcolor-message"></a>\_Messaggio GETTEXTCOLOR TVM

Recupera il colore del testo corrente del controllo. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetTextColor di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore del testo corrente. Se questo valore è-1, il controllo Usa il colore di sistema per il colore del testo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTEXTCOLOR TVM**](tvm-settextcolor.md)
</dt> </dl>

 

