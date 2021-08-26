---
title: TVM_GETITEMRECT messaggio (Commctrl.h)
description: Recupera il rettangolo di delimitazione per un elemento della visualizzazione albero e indica se l'elemento è visibile. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TreeView GetItemRect.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- TVM_GETITEMRECT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6b58ff7d2ce88fd4257ce7db84fa8bd9b4fa2b2d223af03a3f1d57a83c9b9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054001"
---
# <a name="tvm_getitemrect-message"></a>Messaggio TVM \_ GETITEMRECT

Recupera il rettangolo di delimitazione per un elemento della visualizzazione albero e indica se l'elemento è visibile. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TreeView GetItemRect.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica la parte dell'elemento per cui recuperare il rettangolo di delimitazione. Se questo parametro è **TRUE,** il rettangolo di delimitazione include solo il testo dell'elemento. In caso contrario, include l'intera riga che l'elemento occupa nel controllo di visualizzazione albero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che, quando si invia il messaggio, contiene l'handle dell'elemento per il quale recuperare il rettangolo. Per altre informazioni su come inserire l'handle dell'elemento in questo parametro, vedere l'esempio seguente. Dopo la restituzione dal messaggio, questo parametro contiene il rettangolo di delimitazione. Le coordinate sono relative all'angolo superiore sinistro del controllo visualizzazione albero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'elemento è visibile e il rettangolo di delimitazione è stato recuperato correttamente, il valore restituito è **TRUE.** In caso contrario, il messaggio restituisce **FALSE** e non recupera il rettangolo di delimitazione.

## <a name="remarks"></a>Commenti

Quando si invia questo messaggio, il *parametro lParam* contiene l'handle dell'elemento per cui viene recuperato il rettangolo. L'handle viene inserito in *lParam,* come illustrato nell'esempio seguente:


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

