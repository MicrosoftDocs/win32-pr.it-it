---
title: Messaggio LB_FINDSTRINGEXACT (winuser. h)
description: Trova la prima stringa della casella di riepilogo che corrisponde esattamente alla stringa specificata, ad eccezione del fatto che la ricerca non fa distinzione tra maiuscole e minuscole.
ms.assetid: 9bfe21af-626d-4416-aa20-65c425bd99af
keywords:
- Controlli di Windows Message LB_FINDSTRINGEXACT
topic_type:
- apiref
api_name:
- LB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b4f817eabae95c6021647b0c47926b2163722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048712"
---
# <a name="lb_findstringexact-message"></a>\_Messaggio FINDEXACTSTRING lb

Trova la prima stringa della casella di riepilogo che corrisponde esattamente alla stringa specificata, ad eccezione del fatto che la ricerca non fa distinzione tra maiuscole e minuscole.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento che precede il primo elemento da cercare. Quando la ricerca raggiunge la fine della casella di riepilogo, continua a eseguire la ricerca dalla parte superiore della casella di riepilogo all'elemento specificato dal parametro *wParam* . Se *wParam* è-1, viene eseguita la ricerca dell'intera casella di riepilogo dall'inizio.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione null in cui eseguire la ricerca. Per la ricerca non viene fatta distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice in base zero dell'elemento corrispondente o LB \_ Err se la ricerca ha avuto esito negativo.

## <a name="remarks"></a>Commenti

Questa funzione ha esito positivo solo se la stringa specificata e un elemento casella di riepilogo hanno la stessa lunghezza (ad eccezione del valore null alla fine della stringa specificata) e hanno esattamente gli stessi caratteri.

Se la casella di riepilogo ha lo stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , l'azione eseguita da **lb \_ FindExactString** dipende dal fatto che venga usato lo stile di [**\_ ordinamento lbs**](list-box-styles.md) . Se viene usato l' **\_ ordinamento lbs** , il sistema invia messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) al proprietario della casella di riepilogo per determinare l'elemento corrispondente alla stringa specificata. In caso contrario, **lb \_ FindExactString** tenta di trovare un elemento con un valore Long (specificato come parametro *lParam* del messaggio [**lb \_ ADDSTRING**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) ) che corrisponde al parametro *lParam* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_FindString lb**](lb-findstring.md)
</dt> </dl>

 

 





