---
title: LB_SELECTSTRING messaggio (Winuser.h)
description: Cerca in una casella di riepilogo un elemento che inizia con i caratteri in una stringa specificata. Se viene trovato un elemento corrispondente, l'elemento viene selezionato.
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- LB_SELECTSTRING controlli di Windows messaggio
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
ms.openlocfilehash: 848a0935a1ca4d3ce717fecae3de76f57e36091ba084041aa9d012d6318a269a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434081"
---
# <a name="lb_selectstring-message"></a>Messaggio \_ LB SELECTSTRING

Cerca in una casella di riepilogo un elemento che inizia con i caratteri in una stringa specificata. Se viene trovato un elemento corrispondente, l'elemento viene selezionato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento che precede il primo elemento da cercare. Quando la ricerca raggiunge la fine della casella di riepilogo, continua dalla parte superiore della casella di riepilogo fino all'elemento specificato dal *parametro wParam.* Se *wParam* è -1, l'intera casella di riepilogo viene cercata dall'inizio.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione Null che contiene il prefisso per il quale eseguire la ricerca. La ricerca è indipendente dalla distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la ricerca ha esito positivo, il valore restituito è l'indice dell'elemento selezionato. Se la ricerca non riesce, il valore restituito è LB \_ ERR e la selezione corrente non viene modificata.

## <a name="remarks"></a>Commenti

La casella di riepilogo viene scorrendo, se necessario, per visualizzare l'elemento selezionato.

Non usare questo messaggio con una casella di riepilogo con gli stili [**\_ LBS MULTIPLESEL**](list-box-styles.md) o [**\_ LBS EXTENDEDSEL.**](list-box-styles.md)

Un elemento viene selezionato solo se i caratteri iniziali del punto iniziale corrispondono ai caratteri nella stringa specificata dal *parametro lParam.*

Se la casella di riepilogo ha lo stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS di LBS,**](list-box-styles.md) l'azione eseguita da **LB \_ SELECTSTRING** dipende dall'uso o meno dello stile [**\_ LBS SORT.**](list-box-styles.md) Se **si usa \_ LBS SORT,** il sistema invia messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) al proprietario della casella di riepilogo per determinare quale elemento corrisponde alla stringa specificata. In caso contrario, **LB \_ SELECTSTRING** tenta di trovare un elemento con un valore long (fornito come parametro *lParam* del messaggio [**LB \_ ADDSTRING**](lb-addstring.md) o [**LB \_ INSERTSTRING)**](lb-insertstring.md) che corrisponde al *parametro lParam.*

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ FINDSTRING**](lb-findstring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> </dl>

 

 





