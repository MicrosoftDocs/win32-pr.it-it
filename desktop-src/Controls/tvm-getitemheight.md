---
title: Messaggio TVM_GETITEMHEIGHT (COMmctrl. h)
description: Recupera l'altezza corrente di ogni elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemHeight di TreeView.
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- Controlli di Windows Message TVM_GETITEMHEIGHT
topic_type:
- apiref
api_name:
- TVM_GETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789347b7a50f9bb42a7aebb6fecddf24c42c559c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874662"
---
# <a name="tvm_getitemheight-message"></a>\_Messaggio GETITEMHEIGHT TVM

Recupera l'altezza corrente di ogni elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemHeight di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'altezza, in pixel, di ogni elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETITEMHEIGHT TVM**](tvm-setitemheight.md)
</dt> </dl>

 

 





