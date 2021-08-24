---
title: TVM_GETINSERTMARKCOLOR messaggio (Commctrl.h)
description: Recupera il colore utilizzato per disegnare il segno di inserimento per la visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TreeView GetInsertMarkColor.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- TVM_GETINSERTMARKCOLOR dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38c784f6b3c363d68472270f0f52cb97cea7c13b6eb709d1aba4975d3cd97bca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834151"
---
# <a name="tvm_getinsertmarkcolor-message"></a>Messaggio TVM \_ GETINSERTMARKCOLOR

Recupera il colore utilizzato per disegnare il segno di inserimento per la visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ TreeView GetInsertMarkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un [**valore COLORREF**](/windows/desktop/gdi/colorref) che contiene il colore del segno di inserimento corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVM \_ SETINSERTMARKCOLOR**](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

