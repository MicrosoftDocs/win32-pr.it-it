---
title: TVM_ENSUREVISIBLE messaggio (Commctrl.h)
description: Garantisce che un elemento della visualizzazione albero sia visibile, espandendo l'elemento padre o scorrendo il controllo visualizzazione albero, se necessario. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro EnsureVisible di TreeView.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- TVM_ENSUREVISIBLE di Windows di messaggi
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
ms.openlocfilehash: c1072c7213eb2172896980662bcd7a22a3c41fccf34eea2f7a107ab7ff894b32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797251"
---
# <a name="tvm_ensurevisible-message"></a>Messaggio TVM \_ ENSUREVISIBLE

Garantisce che un elemento della visualizzazione albero sia visibile, espandendo l'elemento padre o scorrendo il controllo visualizzazione albero, se necessario. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ EnsureVisible di TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se il sistema ha scorrendo gli elementi nel controllo visualizzazione albero e nessun elemento è stato espanso. In caso contrario, il messaggio restituisce zero.

## <a name="remarks"></a>Commenti

Se il messaggio TVM ENSUREVISIBLE espande l'elemento padre, la finestra padre riceve i codici di notifica \_ [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) e [TVN \_ ITEMEXPANDED.](tvn-itemexpanded.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





