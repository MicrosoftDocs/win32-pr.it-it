---
title: Messaggio CB_SELECTSTRING (winuser. h)
description: Esegue la ricerca nell'elenco di una casella combinata per un elemento che inizia con i caratteri in una stringa specificata. Se viene trovato un elemento corrispondente, questo viene selezionato e copiato nel controllo di modifica.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- Controlli di Windows Message CB_SELECTSTRING
topic_type:
- apiref
api_name:
- CB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2913b95c02cdfd3c7a9c96a8652038a04d8fde8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048349"
---
# <a name="cb_selectstring-message"></a>\_Messaggio SELECTSTRING CB

Esegue la ricerca nell'elenco di una casella combinata per un elemento che inizia con i caratteri in una stringa specificata. Se viene trovato un elemento corrispondente, questo viene selezionato e copiato nel controllo di modifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento che precede il primo elemento da cercare. Quando la ricerca raggiunge la fine dell'elenco, viene proseguita dall'inizio dell'elenco fino all'elemento specificato dal parametro *wParam* . Se *wParam* è-1, viene eseguita una ricerca nell'intero elenco dall'inizio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione null che contiene i caratteri da cercare. Per la ricerca non viene fatta distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la stringa viene trovata, il valore restituito è l'indice dell'elemento selezionato. Se la ricerca ha esito negativo, il valore restituito è CB \_ Err e la selezione corrente non viene modificata.

## <a name="remarks"></a>Commenti

Viene selezionata una stringa solo se i caratteri del punto iniziale corrispondono ai caratteri nella stringa di prefisso.

Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo stile [**CBS \_ HASSTRINGS**](combo-box-styles.md) , il messaggio **\_ SELECTSTRING di CB** dipende dal fatto che si usi lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) . Se viene usato lo stile di **\_ ordinamento CBS** , il sistema invia messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) al proprietario della casella combinata per determinare l'elemento corrispondente alla stringa specificata. Se non si usa lo stile **di \_ ordinamento CBS** , **CB \_ SELECTSTRING** tenta di trovare una corrispondenza tra il valore **DWORD** e il valore del parametro *lParam* .

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

[**CB \_ FindExactString**](cb-findstringexact.md)
</dt> <dt>

[**\_CAcursel CB**](cb-setcursel.md)
</dt> <dt>

[**\_COMPAREITEM WM**](wm-compareitem.md)
</dt> </dl>

 

 





