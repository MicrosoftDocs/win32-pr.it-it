---
title: TVM_GETTEXTCOLOR messaggio (Commctrl.h)
description: Recupera il colore del testo corrente del controllo. È possibile inviare questo messaggio in modo esplicito o usando la macro TreeView \_ GetTextColor.
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- TVM_GETTEXTCOLOR controlli Windows messaggio
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
ms.openlocfilehash: 65a578753b6f86d2ceaa6a664fe6e6e0ff88475dccfb953ae6c6f652bc2dffbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669712"
---
# <a name="tvm_gettextcolor-message"></a>Messaggio TVM \_ GETTEXTCOLOR

Recupera il colore del testo corrente del controllo. È possibile inviare questo messaggio in modo esplicito o usando la macro [**TreeView \_ GetTextColor.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un [**valore COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore del testo corrente. Se questo valore è -1, il controllo usa il colore di sistema per il colore del testo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md)
</dt> </dl>

 

