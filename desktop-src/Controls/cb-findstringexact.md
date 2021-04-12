---
title: Messaggio CB_FINDSTRINGEXACT (winuser. h)
description: Trova la prima stringa della casella di riepilogo in una casella combinata che corrisponde alla stringa specificata nel parametro lParam.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- Controlli di Windows Message CB_FINDSTRINGEXACT
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
ms.openlocfilehash: f70c56a5f13fffa8dfedebd13f9830c62ef941cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519342"
---
# <a name="cb_findstringexact-message"></a>\_Messaggio FINDEXACTSTRING CB

Trova la prima stringa della casella di riepilogo in una casella combinata che corrisponde alla stringa specificata nel parametro *lParam* .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento che precede il primo elemento da cercare. Quando la ricerca raggiunge la fine della casella di riepilogo, continua dalla parte superiore della casella di riepilogo all'elemento specificato dal parametro *wParam* . Se *wParam* è 1, viene eseguita la ricerca dell'intera casella di riepilogo dall'inizio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione null in cui eseguire la ricerca. Per la ricerca non viene fatta distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice in base zero dell'elemento corrispondente. Se la ricerca ha esito negativo, è CB \_ Err.

## <a name="remarks"></a>Commenti

Questa funzione ha esito positivo solo se la stringa specificata e un elemento casella combinata hanno la stessa lunghezza (ad eccezione del carattere di terminazione null) e gli stessi caratteri.

Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo [**stile \_ HASSTRINGS CBS**](combo-box-styles.md) , la funzionalità del **messaggio \_ CB FindExactString** dipende dal fatto che l'applicazione usi lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) . Se si usa lo stile di **\_ ordinamento CBS** , i messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) vengono inviati al proprietario della casella combinata per determinare l'elemento corrispondente alla stringa specificata. Se non si usa lo stile **di \_ ordinamento CBS** , il messaggio **CB \_ FindExactString** Cerca un elemento elenco che corrisponda al valore del parametro *lParam* .

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

[**CB \_ FindString**](cb-findstring.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**\_COMPAREITEM WM**](wm-compareitem.md)
</dt> </dl>

 

 





