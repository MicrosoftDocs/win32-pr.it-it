---
title: Messaggio TVM_SORTCHILDREN (COMmctrl. h)
description: Ordina gli elementi figlio dell'elemento padre specificato in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SortChildren di TreeView.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- Controlli di Windows Message TVM_SORTCHILDREN
topic_type:
- apiref
api_name:
- TVM_SORTCHILDREN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341591c31accb4aab0b49f611359a93ec99c0cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048697"
---
# <a name="tvm_sortchildren-message"></a>\_Messaggio SORTCHILDREN TVM

Ordina gli elementi figlio dell'elemento padre specificato in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SortChildren di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica se l'ordinamento è ricorsivo. Impostare *wParam* su **true** per ordinare tutti i livelli degli elementi figlio sotto l'elemento padre. In caso contrario, vengono ordinati solo gli elementi figlio immediati dell'elemento padre.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elemento padre i cui elementi figlio devono essere ordinati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio dispone gli elementi della struttura ad albero utilizzando [**due**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) sul nome dell'elemento. È possibile usare il messaggio [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) per personalizzare il comportamento di ordinamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

