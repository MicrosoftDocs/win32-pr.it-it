---
title: CB_FINDSTRINGEXACT messaggio (Winuser.h)
description: Trova la prima stringa della casella di riepilogo in una casella combinata che corrisponde alla stringa specificata nel parametro lParam.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- CB_FINDSTRINGEXACT dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- CB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95010548601350b666ee65da4bd048127917dc9c1e80ac26ead844d8597a7a18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079145"
---
# <a name="cb_findstringexact-message"></a>CB \_ FINDSTRINGEXACT message

Trova la prima stringa della casella di riepilogo in una casella combinata che corrisponde alla stringa specificata nel *parametro lParam.*

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento che precede il primo elemento in cui eseguire la ricerca. Quando la ricerca raggiunge la fine della casella di riepilogo, continua dalla parte superiore della casella di riepilogo fino all'elemento specificato dal *parametro wParam.* Se *wParam* è -1, l'intera casella di riepilogo viene cercata dall'inizio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione Null di cui eseguire la ricerca. La ricerca non fa distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice in base zero dell'elemento corrispondente. Se la ricerca ha esito negativo, si tratta di CB \_ ERR.

## <a name="remarks"></a>Commenti

Questa funzione ha esito positivo solo se la stringa specificata e un elemento della casella combinata hanno la stessa lunghezza (ad eccezione del carattere Null di terminazione) e gli stessi caratteri.

Se si crea la casella combinata con uno stile creato dal proprietario ma senza lo stile [**\_ HASSTRINGS di CBS,**](combo-box-styles.md) la funzionalità del messaggio **CB \_ FINDSTRINGEXACT** dipende dal fatto che l'applicazione usi lo stile [**CBS \_ SORT.**](combo-box-styles.md) Se si usa lo **stile SORT di CBS, \_** i messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) vengono inviati al proprietario della casella combinata per determinare quale elemento corrisponde alla stringa specificata. Se non si usa lo stile **SORT di CBS, \_** il messaggio **\_ CB FINDSTRINGEXACT** cerca un elemento di elenco che corrisponda al valore del *parametro lParam.*

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

[**CB \_ FINDSTRING**](cb-findstring.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

 





