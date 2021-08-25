---
title: LB_GETCURSEL messaggio (Winuser.h)
description: Ottiene l'indice dell'elemento attualmente selezionato, se presente, in una casella di riepilogo a selezione singola.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- LB_GETCURSEL dei controlli Windows messaggio
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
ms.openlocfilehash: d67a060669d48a9ab020540c78ece395504c9f0b7e36807e3ac59daf216ea395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085521"
---
# <a name="lb_getcursel-message"></a>Messaggio GETCURSEL di LB \_

Ottiene l'indice dell'elemento attualmente selezionato, se presente, in una casella di riepilogo a selezione singola.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In una casella di riepilogo a selezione singola il valore restituito è l'indice in base zero dell'elemento attualmente selezionato. Se non è presente alcuna selezione, il valore restituito è LB \_ ERR.

## <a name="remarks"></a>Commenti

Per recuperare gli indici degli elementi selezionati in una casella di riepilogo a selezione multipla, usare il [**messaggio \_ LB GETSELITEMS.**](lb-getselitems.md) Per determinare se l'elemento con il rettangolo di attivazione in una casella di riepilogo a selezione multipla è selezionato, usare il [**messaggio \_ LB GETSEL.**](lb-getsel.md)

Se inviato a una casella di riepilogo a selezione multipla, **LB \_ GETCURSEL** restituisce l'indice dell'elemento con il rettangolo di attivazione. Se non è selezionato alcun elemento, restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**LB \_ GETCARETINDEX**](lb-getcaretindex.md)
</dt> <dt>

[**LB \_ GETSEL**](lb-getsel.md)
</dt> <dt>

[**LB \_ GETSELITEMS**](lb-getselitems.md)
</dt> <dt>

[**LB \_ SETCURSEL**](lb-setcursel.md)
</dt> </dl>

 

 





