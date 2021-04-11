---
title: Messaggio CB_FINDSTRING (winuser. h)
description: Cerca nella casella di riepilogo di una casella combinata un elemento che inizia con i caratteri in una stringa specificata.
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- Controlli di Windows Message CB_FINDSTRING
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
ms.openlocfilehash: 295300790a27a956bce953e4e293c07c22ec0d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119738"
---
# <a name="cb_findstring-message"></a>\_Messaggio FindString CB

Cerca nella casella di riepilogo di una casella combinata un elemento che inizia con i caratteri in una stringa specificata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento che precede il primo elemento da cercare. Quando la ricerca raggiunge la fine della casella di riepilogo, continua dalla parte superiore della casella di riepilogo all'elemento specificato dal parametro *wParam* . Se *wParam* è-1, viene eseguita la ricerca dell'intera casella di riepilogo dall'inizio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione null che contiene i caratteri da cercare. Per la ricerca non viene fatta distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice in base zero dell'elemento corrispondente. Se la ricerca ha esito negativo, è CB \_ Err.

## <a name="remarks"></a>Commenti

Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo stile [**CBS \_ HASSTRINGS**](combo-box-styles.md) , il messaggio **\_ FindString di CB** dipende dal fatto che l'applicazione usi lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) . Se si usa lo stile di **\_ ordinamento CBS** , i messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) vengono inviati al proprietario della casella combinata per determinare l'elemento corrispondente alla stringa specificata. Se non si usa lo stile **di \_ ordinamento CBS** , il messaggio **CB \_ FindString** Cerca un elemento elenco che corrisponda al valore del parametro *lParam* .

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

[**CB \_ FindExactString**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**\_CAcursel CB**](cb-setcursel.md)
</dt> <dt>

[**\_COMPAREITEM WM**](wm-compareitem.md)
</dt> </dl>

 

 





