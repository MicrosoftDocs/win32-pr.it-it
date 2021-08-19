---
title: TVM_SETSCROLLTIME messaggio (Commctrl.h)
description: Imposta il tempo di scorrimento massimo per il controllo visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TreeView SetScrollTime.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- TVM_SETSCROLLTIME dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c9ca3392de81a712aa6be7dc2addb87eedf65af4aa77958e5b7f5fbb2eafc87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408488"
---
# <a name="tvm_setscrolltime-message"></a>Messaggio \_ TVM SETSCROLLTIME

Imposta il tempo di scorrimento massimo per il controllo visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TreeView SetScrollTime.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Nuovo tempo massimo di scorrimento, espresso in millisecondi.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il tempo massimo di scorrimento precedente, espresso in millisecondi.

## <a name="remarks"></a>Commenti

Il tempo di scorrimento massimo è il periodo di tempo più lungo che può essere necessario per un'operazione di scorrimento. Lo scorrimento verrà regolato in modo che lo scorrimento si scorrono entro il tempo di scorrimento massimo. Un'operazione di scorrimento può richiedere meno tempo del valore massimo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVM \_ GETSCROLLTIME**](tvm-getscrolltime.md)
</dt> </dl>

 

 





