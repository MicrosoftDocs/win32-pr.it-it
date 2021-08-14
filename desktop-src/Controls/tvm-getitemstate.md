---
title: TVM_GETITEMSTATE messaggio (Commctrl.h)
description: Recupera alcuni o tutti gli attributi di stato di un elemento della visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemState di TreeView.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- TVM_GETITEMSTATE controlli di Windows messaggio
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff562af5a97684caa3e5b17ab47d0f67f82a6789e2510cf1598a3189073fda81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261261"
---
# <a name="tvm_getitemstate-message"></a>Messaggio TVM \_ GETITEMSTATE

Recupera alcuni o tutti gli attributi di stato di un elemento della visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemState di TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per l'elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Maschera utilizzata per specificare gli stati per cui eseguire una query. Equivale al membro **stateMask** di [**TVITEMEX.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore UINT** con i bit di stato appropriati impostati su **TRUE.** Verranno impostati solo i bit specificati da *lParam* e che sono **TRUE.** Questo valore è equivalente al **membro di** stato di [**TVITEMEX.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





