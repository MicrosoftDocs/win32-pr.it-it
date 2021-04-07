---
title: Messaggio TVM_ENSUREVISIBLE (COMmctrl. h)
description: Garantisce che un elemento della visualizzazione struttura ad albero sia visibile, espandendo l'elemento padre o scorrendo il controllo di visualizzazione albero, se necessario. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro EnsureVisible di TreeView.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- Controlli di Windows Message TVM_ENSUREVISIBLE
topic_type:
- apiref
api_name:
- TVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06100ee33106736076608aa216d2aebc03b76ebe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964033"
---
# <a name="tvm_ensurevisible-message"></a>\_Messaggio ENSUREVISIBLE TVM

Garantisce che un elemento della visualizzazione struttura ad albero sia visibile, espandendo l'elemento padre o scorrendo il controllo di visualizzazione albero, se necessario. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ EnsureVisible di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se il sistema ha eseguito lo scorrimento degli elementi nel controllo di visualizzazione albero e nessun elemento è stato espanso. In caso contrario, il messaggio restituisce zero.

## <a name="remarks"></a>Commenti

Se il \_ messaggio TVM ENSUREVISIBLE espande l'elemento padre, la finestra padre riceve i codici di notifica [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) e [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





