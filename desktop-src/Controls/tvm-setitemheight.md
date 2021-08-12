---
title: TVM_SETITEMHEIGHT messaggio (Commctrl.h)
description: Imposta l'altezza degli elementi della visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TreeView SetItemHeight.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- TVM_SETITEMHEIGHT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9afff57188a9683d18c6bff780b4a9f61479526d44ea77985742520a47e66cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669646"
---
# <a name="tvm_setitemheight-message"></a>Messaggio \_ TVM SETITEMHEIGHT

Imposta l'altezza degli elementi della visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TreeView SetItemHeight.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Nuova altezza di ogni elemento nella visualizzazione albero, in pixel. Le altezze minori di 1 verranno impostate su 1. Se questo argomento non è pari e il controllo visualizzazione albero non ha lo stile [**\_ TVS NONEVENHEIGHT,**](tree-view-control-window-styles.md) questo valore verrà arrotondato per esere al valore pari più vicino. Se questo argomento è -1, il controllo ripristina l'altezza predefinita dell'elemento.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'altezza precedente degli elementi, in pixel.

## <a name="remarks"></a>Commenti

Il controllo di visualizzazione albero usa questo valore per l'altezza di tutti gli elementi. Per modificare l'altezza dei singoli elementi, vedere la descrizione del membro **iIntegral** della [**struttura TVITEMEX.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVM \_ GETITEMHEIGHT**](tvm-getitemheight.md)
</dt> </dl>

 

 





