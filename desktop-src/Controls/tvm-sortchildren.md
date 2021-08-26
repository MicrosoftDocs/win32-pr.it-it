---
title: TVM_SORTCHILDREN messaggio (Commctrl.h)
description: Ordina gli elementi figlio dell'elemento padre specificato in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro SortChildren di TreeView.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- TVM_SORTCHILDREN di controllo Windows messaggio
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
ms.openlocfilehash: f975814fadc5271c562e4e8e420c35dbb3450142bed797af83af73fdf81a55d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913801"
---
# <a name="tvm_sortchildren-message"></a>Messaggio \_ TVM SORTCHILDREN

Ordina gli elementi figlio dell'elemento padre specificato in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ SortChildren di TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica se l'ordinamento è ricorsivo. Impostare *wParam* su **TRUE per** ordinare tutti i livelli di elementi figlio sotto l'elemento padre. In caso contrario, vengono ordinati solo gli elementi figlio immediati dell'elemento padre.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elemento padre i cui elementi figlio devono essere ordinati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio consente di alfabeticizzare gli elementi della struttura ad albero [**usando lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) sul nome dell'elemento. È possibile usare il [**messaggio TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) per personalizzare il comportamento di ordinamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

