---
title: CB_FINDSTRINGEXACT messaggio (Winuser.h)
description: Trova la prima stringa della casella di riepilogo in una casella combinata che corrisponde alla stringa specificata nel parametro lParam.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- CB_FINDSTRINGEXACT messaggio Controlli Windows
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
ms.openlocfilehash: 7f99d85c7dddb95bdfb168443d6f977c22273a87
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327176"
---
# <a name="cb_findstringexact-message"></a>Messaggio CB \_ FINDSTRINGEXACT

Trova la prima stringa della casella di riepilogo in una casella combinata che corrisponde alla stringa specificata nel *parametro lParam.*

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento che precede il primo elemento in cui eseguire la ricerca. Quando la ricerca raggiunge la parte inferiore della casella di riepilogo, continua dalla parte superiore della casella di riepilogo all'elemento specificato dal *parametro wParam.* Se *wParam è* -1, l'intera casella di riepilogo viene cercata dall'inizio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione Null in cui eseguire la ricerca. La ricerca non fa distinzione tra maiuscole e minuscole, quindi questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice in base zero dell'elemento corrispondente. Se la ricerca ha esito negativo, si tratta di CB \_ ERR.

## <a name="remarks"></a>Commenti

Questa funzione ha esito positivo solo se la stringa specificata e un elemento della casella combinata hanno la stessa lunghezza (ad eccezione del carattere Null di terminazione) e degli stessi caratteri.

Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo stile [**\_ CBS HASSTRINGS,**](combo-box-styles.md) la funzionalità del messaggio **CB \_ FINDSTRINGEXACT** dipende dal fatto che l'applicazione usi lo stile [**CBS \_ SORT.**](combo-box-styles.md) Se si usa lo **stile CBS \_ SORT,** i messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) vengono inviati al proprietario della casella combinata per determinare quale elemento corrisponde alla stringa specificata. Se non si usa lo stile **CBS \_ SORT,** il messaggio **CB \_ FINDSTRINGEXACT** cerca un elemento dell'elenco che corrisponde al valore del *parametro lParam.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                                           |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                     |
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

 

 





