---
title: Messaggio LB_SETCARETINDEX (winuser. h)
description: Imposta il rettangolo di attivazione sull'elemento in corrispondenza dell'indice specificato in una casella di riepilogo a selezione multipla. Se l'elemento non è visibile, viene spostato nella visualizzazione.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- Controlli di Windows Message LB_SETCARETINDEX
topic_type:
- apiref
api_name:
- LB_SETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857e5c2637e5bcc90b2c60bfd8295a91ff297fb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874341"
---
# <a name="lb_setcaretindex-message"></a>\_Messaggio SETCARETINDEX lb

Imposta il rettangolo di attivazione sull'elemento in corrispondenza dell'indice specificato in una casella di riepilogo a selezione multipla. Se l'elemento non è visibile, viene spostato nella visualizzazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice in base zero dell'elemento della casella di riepilogo che deve ricevere il rettangolo di attivazione.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Se questo valore è **false**, l'elemento viene spostato fino a quando non è completamente visibile; Se è **true**, l'elemento viene sottoposta a scorrimento fino a quando non è visibile almeno parzialmente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è LB \_ Err (-1). In caso contrario, \_ viene restituito lb OK (0).

## <a name="remarks"></a>Commenti

Se questo messaggio viene inviato a una casella di riepilogo a selezione singola che non contiene un elemento selezionato, l'indice del cursore viene impostato sull'elemento specificato dal parametro *wParam* . Se la casella di riepilogo a selezione singola contiene un elemento selezionato, la casella di riepilogo restituisce LB \_ Err.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETCARETINDEX lb**](lb-getcaretindex.md)
</dt> </dl>

 

 





