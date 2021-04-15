---
title: Messaggio TVM_DELETEITEM (COMmctrl. h)
description: Rimuove un elemento e tutti i relativi elementi figlio da un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro DeleteItem di TreeView.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- Controlli di Windows Message TVM_DELETEITEM
topic_type:
- apiref
api_name:
- TVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8783fd5acdf7319699cdc67cbb3ea075e4dbbc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476954"
---
# <a name="tvm_deleteitem-message"></a>\_Messaggio DeleteItem TVM

Rimuove un elemento e tutti i relativi elementi figlio da un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ DeleteItem di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle **HTREEITEM** per l'elemento da eliminare. Se *lParam* è impostato sulla \_ radice TVI o su **null**, tutti gli elementi vengono eliminati. È anche possibile usare la [**macro \_ DeleteAllItems di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) per eliminare tutti gli elementi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Non è sicuro eliminare gli elementi in risposta a una notifica, ad esempio [TVN \_ SELCHANGING](tvn-selchanging.md).

Dopo che un elemento è stato eliminato, il relativo handle non è valido e non può essere utilizzato.

La finestra padre riceve un codice di notifica [ \_ DeleteItem di TVN](tvn-deleteitem.md) quando ogni elemento viene rimosso.

Se l'etichetta dell'elemento viene modificata, l'operazione di modifica viene annullata e la finestra padre riceve il codice di notifica [ \_ ENDLABELEDIT di TVN](tvn-endlabeledit.md) .

Se si eliminano tutti gli elementi di un controllo di visualizzazione albero con lo stile [**\_ NoScroll TV**](tree-view-control-window-styles.md) , gli elementi aggiunti successivamente potrebbero non essere visualizzati correttamente. Per ulteriori informazioni, vedere [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





