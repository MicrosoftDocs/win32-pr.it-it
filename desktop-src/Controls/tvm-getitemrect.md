---
title: Messaggio TVM_GETITEMRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione per un elemento della visualizzazione struttura ad albero e indica se l'elemento è visibile. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemRect di TreeView.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- Controlli di Windows Message TVM_GETITEMRECT
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
ms.openlocfilehash: ebdf4d73fb83ddbd8e9e682f11ee1f5ecfbd5153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119567"
---
# <a name="tvm_getitemrect-message"></a>\_Messaggio GETITEMRECT TVM

Recupera il rettangolo di delimitazione per un elemento della visualizzazione struttura ad albero e indica se l'elemento è visibile. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemRect di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica la parte dell'elemento per la quale recuperare il rettangolo di delimitazione. Se questo parametro è **true**, il rettangolo di delimitazione include solo il testo dell'elemento. In caso contrario, include l'intera riga occupata dall'elemento nel controllo di visualizzazione albero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che, quando invia il messaggio, contiene l'handle dell'elemento per il quale recuperare il rettangolo. Vedere l'esempio seguente per altre informazioni su come inserire l'handle di elemento in questo parametro. Dopo la restituzione dal messaggio, questo parametro contiene il rettangolo di delimitazione. Le coordinate sono relative all'angolo superiore sinistro del controllo di visualizzazione ad albero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'elemento è visibile e il rettangolo di delimitazione è stato recuperato correttamente, il valore restituito è **true**. In caso contrario, il messaggio restituisce **false** e non recupera il rettangolo di delimitazione.

## <a name="remarks"></a>Commenti

Quando si invia questo messaggio, il parametro *lParam* contiene l'handle dell'elemento per il quale viene recuperato il rettangolo. L'handle viene inserito in *lParam* come illustrato nell'esempio seguente:


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

