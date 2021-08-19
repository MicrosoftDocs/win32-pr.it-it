---
title: TVM_DELETEITEM messaggio (Commctrl.h)
description: Rimuove un elemento e tutti i relativi elementi figlio da un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la macro TreeView \_ DeleteItem.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- TVM_DELETEITEM dei messaggi Windows controlli
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
ms.openlocfilehash: 7ef0165ffaf1f0f04b32cda43e21c97fed012ad6d61b32f8919612f8924f7c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018689"
---
# <a name="tvm_deleteitem-message"></a>Messaggio TVM \_ DELETEITEM

Rimuove un elemento e tutti i relativi elementi figlio da un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**TreeView \_ DeleteItem.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

**Handle HTREEITEM** per l'elemento da eliminare. Se *lParam è* impostato su TVI \_ ROOT o su **NULL,** tutti gli elementi vengono eliminati. È anche possibile usare la macro [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) per eliminare tutti gli elementi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Non è sicuro eliminare elementi in risposta a una notifica, ad esempio [TVN \_ SELCHANGING](tvn-selchanging.md).

Dopo l'eliminazione di un elemento, l'handle non è valido e non può essere usato.

La finestra padre riceve un [codice di notifica TVN \_ DELETEITEM](tvn-deleteitem.md) quando ogni elemento viene rimosso.

Se l'etichetta dell'elemento viene modificata, l'operazione di modifica viene annullata e la finestra padre riceve il codice di notifica [ \_ TVN ENDLABELEDIT.](tvn-endlabeledit.md)

Se si eliminano tutti gli elementi in un controllo di visualizzazione albero con lo stile [**\_ TVS NOSCROLL,**](tree-view-control-window-styles.md) gli elementi aggiunti successivamente potrebbero non essere visualizzati correttamente. Per altre informazioni, vedere [**TreeView \_ DeleteAllItems.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





