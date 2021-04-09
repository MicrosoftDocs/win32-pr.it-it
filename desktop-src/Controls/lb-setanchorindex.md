---
title: Messaggio LB_SETANCHORINDEX (winuser. h)
description: Imposta l'elemento di ancoraggio \ 8212, ovvero l'elemento da cui inizia una selezione multipla. Una selezione multipla si estende a tutti gli elementi dall'elemento di ancoraggio all'elemento del punto di inserimento.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setanchorindex.htm
keywords:
- Controlli di Windows Message LB_SETANCHORINDEX
topic_type:
- apiref
api_name:
- LB_SETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3ac2aa8798d0e13d8191f630fef7f54f510ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121010"
---
# <a name="lb_setanchorindex-message"></a>\_Messaggio SETANCHORINDEX lb

Imposta l'elemento di ancoraggio, ovvero l'elemento da cui inizia una selezione multipla. Una selezione multipla si estende a tutti gli elementi dall'elemento di ancoraggio all'elemento del punto di inserimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice del nuovo elemento di ancoraggio.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è zero.

Se il messaggio ha esito negativo, il valore restituito è LB \_ Err.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETANCHORINDEX lb**](lb-getanchorindex.md)
</dt> </dl>

 

 





