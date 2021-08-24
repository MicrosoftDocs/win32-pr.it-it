---
title: TVM_SETINSERTMARKCOLOR messaggio (Commctrl.h)
description: Imposta il colore utilizzato per disegnare il segno di inserimento per la visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TreeView SetInsertMarkColor.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- TVM_SETINSERTMARKCOLOR controlli Windows messaggio
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
ms.openlocfilehash: 05d5fd9984b77c99a13e1c7eab24c231e0ce7f601ecb79f8747cdf7ea3011327
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636761"
---
# <a name="tvm_setinsertmarkcolor-message"></a>Messaggio \_ TVM SETINSERTMARKCOLOR

Imposta il colore utilizzato per disegnare il segno di inserimento per la visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TreeView SetInsertMarkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

[**Valore COLORREF**](/windows/desktop/gdi/colorref) che contiene il nuovo colore del segno di inserimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore COLORREF** che contiene il colore del segno di inserimento precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVM \_ GETINSERTMARKCOLOR**](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

