---
title: TVM_GETBKCOLOR messaggio (Commctrl.h)
description: Recupera il colore di sfondo corrente del controllo . È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TreeView GetBkColor.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- TVM_GETBKCOLOR di controllo Windows messaggio
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
ms.openlocfilehash: 8a5a6530b1aada1fab06c0b353d7ead666e61f0f796b890d1f5c56fe0be094b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088451"
---
# <a name="tvm_getbkcolor-message"></a>Messaggio TVM \_ GETBKCOLOR

Recupera il colore di sfondo corrente del controllo . È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ TreeView GetBkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un [**valore COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore di sfondo corrente. Se questo valore è -1, il controllo usa il colore di sistema per il colore di sfondo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVM \_ SETBKCOLOR**](tvm-setbkcolor.md)
</dt> </dl>

 

