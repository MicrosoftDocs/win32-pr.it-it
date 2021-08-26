---
title: TVM_INSERTITEM messaggio (Commctrl.h)
description: Inserisce un nuovo elemento in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro InsertItem di TreeView.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- TVM_INSERTITEM controlli Windows messaggio
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f8a324613820b94e0bd2c49d8fa78136038471f820dd2b9ed8e38ace15f0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060191"
---
# <a name="tvm_insertitem-message"></a>Messaggio \_ INSERTITEM TVM

Inserisce un nuovo elemento in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ InsertItem di TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) che specifica gli attributi dell'elemento della visualizzazione albero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **l'handle HTREEITEM** al nuovo elemento in caso di esito positivo oppure **NULL in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVM \_ INSERTITEMW** (Unicode) e **TVM \_ INSERTITEMA** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[TVN \_ ENDLABELEDIT](tvn-endlabeledit.md)
</dt> </dl>

 

 





