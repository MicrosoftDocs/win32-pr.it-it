---
title: Messaggio LB_GETCURSEL (winuser. h)
description: Ottiene l'indice dell'elemento attualmente selezionato, se presente, in una casella di riepilogo a selezione singola.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- Controlli di Windows Message LB_GETCURSEL
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6209f1f5b67e059f9a2b8a224e6f96ec671e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048709"
---
# <a name="lb_getcursel-message"></a>LB- \_ messaggio GETcursel

Ottiene l'indice dell'elemento attualmente selezionato, se presente, in una casella di riepilogo a selezione singola.

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

In una casella di riepilogo a selezione singola, il valore restituito è l'indice in base zero dell'elemento attualmente selezionato. Se non è presente alcuna selezione, il valore restituito è LB \_ Err.

## <a name="remarks"></a>Commenti

Per recuperare gli indici degli elementi selezionati in una casella di riepilogo a selezione multipla, usare il messaggio [**lb \_ GETSELITEMS**](lb-getselitems.md) . Per determinare se l'elemento con il rettangolo di attivazione in una casella di riepilogo a selezione multipla è selezionato, usare il messaggio [**lb \_ GETSEL**](lb-getsel.md) .

Se viene inviato a una casella di riepilogo a selezione multipla, **lb \_ GetCurSel** restituisce l'indice dell'elemento con il rettangolo di attivazione. Se non è selezionato alcun elemento, viene restituito zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_GETCARETINDEX lb**](lb-getcaretindex.md)
</dt> <dt>

[**\_GETSEL lb**](lb-getsel.md)
</dt> <dt>

[**\_GETSELITEMS lb**](lb-getselitems.md)
</dt> <dt>

[**di \_ lb**](lb-setcursel.md)
</dt> </dl>

 

 





