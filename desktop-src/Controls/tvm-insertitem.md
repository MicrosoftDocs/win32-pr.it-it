---
title: Messaggio TVM_INSERTITEM (COMmctrl. h)
description: Inserisce un nuovo elemento in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TreeView InsertItem.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- Controlli di Windows Message TVM_INSERTITEM
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
ms.openlocfilehash: 719de4c2391ff924c9f6deb8cb4206cfdb56c3ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873517"
---
# <a name="tvm_insertitem-message"></a>\_Messaggio INSERTITEM INSERTITEM

Inserisce un nuovo elemento in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TreeView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) che specifica gli attributi dell'elemento della visualizzazione albero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle **HTREEITEM** al nuovo elemento in caso di esito positivo; in caso contrario, **null** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVM \_ INSERTITEMW** (Unicode) e **TVM \_ INSERTITEMA** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_ENDLABELEDIT TVN](tvn-endlabeledit.md)
</dt> </dl>

 

 





