---
title: Messaggio TVM_SETTEXTCOLOR (COMmctrl. h)
description: Imposta il colore del testo del controllo. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetTextColor di TreeView.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- Controlli di Windows Message TVM_SETTEXTCOLOR
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741999"
---
# <a name="tvm_settextcolor-message"></a>\_Messaggio SETTEXTCOLOR TVM

Imposta il colore del testo del controllo. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetTextColor di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore di [**COLORREF**](/windows/desktop/gdi/colorref) che contiene il nuovo colore del testo. Se questo argomento è-1, il controllo verrà ripristinato utilizzando il colore di sistema per il colore del testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **COLORREF** che rappresenta il colore del testo precedente. Se questo valore è-1, il controllo Usa il colore di sistema per il colore del testo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETTEXTCOLOR TVM**](tvm-gettextcolor.md)
</dt> </dl>

 

