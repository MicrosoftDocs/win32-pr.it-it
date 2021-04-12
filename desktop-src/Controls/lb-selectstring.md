---
title: Messaggio LB_SELECTSTRING (winuser. h)
description: Cerca un elemento in una casella di riepilogo che inizia con i caratteri di una stringa specificata. Se viene trovato un elemento corrispondente, l'elemento viene selezionato.
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- Controlli di Windows Message LB_SELECTSTRING
topic_type:
- apiref
api_name:
- LB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5963ea6530038e17bc7f23d9ab66eba14ca0b05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478550"
---
# <a name="lb_selectstring-message"></a>\_Messaggio SELECTSTRING lb

Cerca un elemento in una casella di riepilogo che inizia con i caratteri di una stringa specificata. Se viene trovato un elemento corrispondente, l'elemento viene selezionato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento che precede il primo elemento da cercare. Quando la ricerca raggiunge la fine della casella di riepilogo, continua dalla parte superiore della casella di riepilogo all'elemento specificato dal parametro *wParam* . Se *wParam* è-1, viene eseguita la ricerca dell'intera casella di riepilogo dall'inizio.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione null che contiene il prefisso per il quale eseguire la ricerca. La ricerca è indipendente dalla distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la ricerca ha esito positivo, il valore restituito è l'indice dell'elemento selezionato. Se la ricerca ha esito negativo, il valore restituito è LB \_ Err e la selezione corrente non viene modificata.

## <a name="remarks"></a>Commenti

Se necessario, viene visualizzata la casella di riepilogo per visualizzare l'elemento selezionato.

Non usare questo messaggio con una casella di riepilogo con gli stili [**\_ MULTIPLESEL lbs**](list-box-styles.md) o [**\_ EXTENDEDSEL lbs**](list-box-styles.md) .

Un elemento viene selezionato solo se i caratteri iniziali dal punto iniziale corrispondono ai caratteri nella stringa specificata dal parametro *lParam* .

Se la casella di riepilogo ha lo stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , l'azione eseguita da **lb \_ SELECTSTRING** dipende dal fatto che venga usato lo stile di [**\_ ordinamento lbs**](list-box-styles.md) . Se viene usato l' **\_ ordinamento lbs** , il sistema invia messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) al proprietario della casella di riepilogo per determinare l'elemento corrispondente alla stringa specificata. In caso contrario, **lb \_ SELECTSTRING** tenta di trovare un elemento con un valore Long (specificato come parametro *lParam* del messaggio [**lb \_ ADDSTRING**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) ) che corrisponde al parametro *lParam* .

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

[**\_ADDSTRING lb**](lb-addstring.md)
</dt> <dt>

[**\_FindString lb**](lb-findstring.md)
</dt> <dt>

[**\_INSERTSTRING lb**](lb-insertstring.md)
</dt> </dl>

 

 





