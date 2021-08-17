---
title: TVM_GETSCROLLTIME messaggio (Commctrl.h)
description: Recupera il tempo di scorrimento massimo per il controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetScrollTime di TreeView.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- TVM_GETSCROLLTIME dei messaggi Windows
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e026a463476d5625f7632d7b6679ce94ca2c8ab6d8c6a050d8938bd46d9858b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408498"
---
# <a name="tvm_getscrolltime-message"></a>Messaggio TVM \_ GETSCROLLTIME

Recupera il tempo di scorrimento massimo per il controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetScrollTime di TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il tempo di scorrimento massimo, in millisecondi.

## <a name="remarks"></a>Commenti

Il tempo di scorrimento massimo è la quantità di tempo massima che un'operazione di scorrimento può richiedere. Lo scorrimento verrà regolato in modo che lo scorrimento si scorrono entro il tempo di scorrimento massimo. Un'operazione di scorrimento può richiedere meno tempo rispetto al valore massimo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVM \_ SETSCROLLTIME**](tvm-setscrolltime.md)
</dt> </dl>

 

 





