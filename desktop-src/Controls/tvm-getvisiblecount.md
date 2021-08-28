---
title: TVM_GETVISIBLECOUNT messaggio (Commctrl.h)
description: Ottiene il numero di elementi che possono essere completamente visibili nella finestra client di un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetVisibleCount di TreeView.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- TVM_GETVISIBLECOUNT controlli Windows messaggio
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07604eed3d3ece140d33bb9c612a2f898f6de02785f2c9916332de60358693fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698661"
---
# <a name="tvm_getvisiblecount-message"></a>Messaggio TVM \_ GETVISIBLECOUNT

Ottiene il numero di elementi che possono essere completamente visibili nella finestra client di un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetVisibleCount di TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di elementi che possono essere completamente visibili nella finestra client del controllo di visualizzazione albero.

## <a name="remarks"></a>Commenti

Il numero di elementi che possono essere completamente visibili può essere maggiore del numero di elementi nel controllo . Il controllo calcola questo valore dividendo l'altezza della finestra client per l'altezza di un elemento.

Si noti che il valore restituito è il numero di elementi che possono essere *completamente* visibili. Se è possibile visualizzare tutti e 20 gli elementi e parte di un altro elemento, il valore restituito è 20.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





