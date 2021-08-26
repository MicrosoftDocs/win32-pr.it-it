---
title: CB_FINDSTRING messaggio (Winuser.h)
description: Cerca nella casella di riepilogo di una casella combinata un elemento che inizia con i caratteri in una stringa specificata.
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- CB_FINDSTRING di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1af584e04a108c39a76a54c05c311d26e107c132d0c132e7b8fcc99a7cd7321b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089355"
---
# <a name="cb_findstring-message"></a>CB \_ FINDSTRING message

Cerca nella casella di riepilogo di una casella combinata un elemento che inizia con i caratteri in una stringa specificata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento che precede il primo elemento in cui eseguire la ricerca. Quando la ricerca raggiunge la fine della casella di riepilogo, continua dalla parte superiore della casella di riepilogo fino all'elemento specificato dal *parametro wParam.* Se *wParam* è -1, l'intera casella di riepilogo viene cercata dall'inizio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione Null che contiene i caratteri da cercare. La ricerca non fa distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice in base zero dell'elemento corrispondente. Se la ricerca ha esito negativo, si tratta di CB \_ ERR.

## <a name="remarks"></a>Commenti

Se si crea la casella combinata con uno stile creato dal proprietario ma senza lo stile [**\_ HASSTRINGS di CBS,**](combo-box-styles.md) le attività del messaggio **\_ CB FINDSTRING** dipendono dal fatto che l'applicazione usi lo stile [**CBS \_ SORT.**](combo-box-styles.md) Se si usa lo **stile SORT di CBS, \_** i messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) vengono inviati al proprietario della casella combinata per determinare quale elemento corrisponde alla stringa specificata. Se non si usa lo stile **CBS \_ SORT,** il messaggio **\_ CB FINDSTRING** cerca un elemento dell'elenco che corrisponda al valore del *parametro lParam.*

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

[**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

 





