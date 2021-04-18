---
title: Messaggio TVM_SETSCROLLTIME (COMmctrl. h)
description: Imposta il tempo massimo di scorrimento per il controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetScrollTime di TreeView.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- Controlli di Windows Message TVM_SETSCROLLTIME
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
ms.openlocfilehash: b49fab2f662b5ec641d9ffc6cc276f2196d2613e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301834"
---
# <a name="tvm_setscrolltime-message"></a>\_Messaggio SETSCROLLTIME TVM

Imposta il tempo massimo di scorrimento per il controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetScrollTime di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Nuovo tempo di scorrimento massimo, in millisecondi.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il tempo di scorrimento massimo precedente, in millisecondi.

## <a name="remarks"></a>Commenti

Il tempo massimo di scorrimento è la quantità di tempo più lungo che può essere eseguita da un'operazione di scorrimento. Lo scorrimento viene regolato in modo che lo scorrimento avvenga entro il tempo massimo di scorrimento. Un'operazione di scorrimento potrebbe richiedere meno tempo rispetto al valore massimo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETSCROLLTIME TVM**](tvm-getscrolltime.md)
</dt> </dl>

 

 





