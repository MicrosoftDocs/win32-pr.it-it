---
title: Messaggio TVM_GETITEMSTATE (COMmctrl. h)
description: Recupera alcuni o tutti gli attributi di stato di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemState di TreeView.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- Controlli di Windows Message TVM_GETITEMSTATE
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
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048544"
---
# <a name="tvm_getitemstate-message"></a>\_Messaggio GETITEMSTATE TVM

Recupera alcuni o tutti gli attributi di stato di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemState di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per l'elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Maschera utilizzata per specificare gli stati in cui eseguire una query. Equivale al membro **stateMask** di [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **uint** con i bit di stato appropriati impostati su **true**. Verranno impostati solo i bit specificati da *lParam* e che sono **true** . Questo valore è equivalente al membro di **stato** di [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





