---
title: CB_SELECTSTRING messaggio (Winuser.h)
description: Cerca nell'elenco di una casella combinata un elemento che inizia con i caratteri in una stringa specificata. Se viene trovato un elemento corrispondente, viene selezionato e copiato nel controllo di modifica.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- CB_SELECTSTRING di controllo Windows messaggio
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
ms.openlocfilehash: 4bedef20646664e37405c97a97f9e49147cad8acc08c05e33172e44a34298f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019969"
---
# <a name="cb_selectstring-message"></a>CB \_ SELECTSTRING message

Cerca nell'elenco di una casella combinata un elemento che inizia con i caratteri in una stringa specificata. Se viene trovato un elemento corrispondente, viene selezionato e copiato nel controllo di modifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento che precede il primo elemento in cui eseguire la ricerca. Quando la ricerca raggiunge la fine dell'elenco, continua dall'inizio dell'elenco all'elemento specificato dal *parametro wParam.* Se *wParam* è -1, viene cercato l'intero elenco dall'inizio.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione Null che contiene i caratteri da cercare. La ricerca non fa distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la stringa viene trovata, il valore restituito è l'indice dell'elemento selezionato. Se la ricerca non riesce, il valore restituito è CB \_ ERR e la selezione corrente non viene modificata.

## <a name="remarks"></a>Commenti

Viene selezionata una stringa solo se i caratteri del punto iniziale corrispondono ai caratteri nella stringa di prefisso.

Se si crea la casella combinata con uno stile creato dal proprietario ma senza lo stile [**\_ CBS HASSTRINGS,**](combo-box-styles.md) l'operazione del messaggio **\_ CB SELECTSTRING** dipende dall'uso o meno dello stile [**CBS \_ SORT.**](combo-box-styles.md) Se si usa lo stile SORT di **CBS, \_** il sistema invia messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) al proprietario della casella combinata per determinare quale elemento corrisponde alla stringa specificata. Se non si usa lo stile **SORT \_ di CBS,** **CB \_ SELECTSTRING** tenta di trovare una corrispondenza tra il valore **DWORD** e il valore del *parametro lParam.*

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

[**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

 





