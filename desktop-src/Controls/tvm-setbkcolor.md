---
title: TVM_SETBKCOLOR messaggio (Commctrl.h)
description: Imposta il colore di sfondo del controllo. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TreeView SetBkColor.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- TVM_SETBKCOLOR dei messaggi Windows controllo
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
ms.openlocfilehash: 0609a15be2b8e05b1f8ca8f4f999cd4888ee946969c25f5bc1d86420b7529f2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060121"
---
# <a name="tvm_setbkcolor-message"></a>Messaggio \_ TVM SETBKCOLOR

Imposta il colore di sfondo del controllo. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ TreeView SetBkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

[**Valore COLORREF**](/windows/desktop/gdi/colorref) che contiene il nuovo colore di sfondo. Se questo valore è -1, il controllo tornerà a usare il colore di sistema per il colore di sfondo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un [**valore COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore di sfondo precedente. Se questo valore è -1, il controllo usava il colore di sistema per il colore di sfondo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVM \_ GETBKCOLOR**](tvm-getbkcolor.md)
</dt> </dl>

 

