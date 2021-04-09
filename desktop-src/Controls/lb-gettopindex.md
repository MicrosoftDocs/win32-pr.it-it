---
title: Messaggio LB_GETTOPINDEX (winuser. h)
description: Ottiene l'indice del primo elemento visibile in una casella di riepilogo.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- Controlli di Windows Message LB_GETTOPINDEX
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdeca8e3f40ab3105bb9703db9355d09a214f5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964257"
---
# <a name="lb_gettopindex-message"></a>\_Messaggio GETTOPINDEX lb

Ottiene l'indice del primo elemento visibile in una casella di riepilogo. Inizialmente l'elemento con indice 0 si trova nella parte superiore della casella di riepilogo, ma se il contenuto della casella di riepilogo è stato spostato, un altro elemento potrebbe trovarsi nella parte superiore. Il primo elemento visibile in una casella di riepilogo a più colonne è l'elemento in alto a sinistra.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice del primo elemento visibile nella casella di riepilogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTOPINDEX lb**](lb-settopindex.md)
</dt> </dl>

 

 





