---
title: LB_FINDSTRING messaggio (Winuser.h)
description: Trova la prima stringa in una casella di riepilogo che inizia con la stringa specificata.
ms.assetid: 1b7f25a7-0892-4d12-b3e3-21180d9ddfb1
keywords:
- LB_FINDSTRING di windows del messaggio
topic_type:
- apiref
api_name:
- LB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a4eb2abbff27c6bde6a4bb44d0faa192ca75229be657bd787aa437b243cd59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671304"
---
# <a name="lb_findstring-message"></a>Messaggio \_ LB FINDSTRING

Trova la prima stringa in una casella di riepilogo che inizia con la stringa specificata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento che precede il primo elemento da cercare. Quando la ricerca raggiunge la fine della casella di riepilogo, continua la ricerca dalla parte superiore della casella di riepilogo all'elemento specificato dal *parametro wParam.* Se *wParam* è -1, l'intera casella di riepilogo viene cercata dall'inizio.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione Null che contiene la stringa da cercare. La ricerca è indipendente dalla distinzione tra maiuscole e minuscole, pertanto questa stringa può contenere qualsiasi combinazione di lettere maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice dell'elemento corrispondente oppure LB \_ ERR se la ricerca non è riuscita.

## <a name="remarks"></a>Commenti

Se la casella di riepilogo ha lo stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS di LBS,**](list-box-styles.md) l'azione eseguita da **LB \_ FINDSTRING** dipende dall'uso o meno dello stile [**\_ LBS SORT.**](list-box-styles.md) Se **si usa \_ LBS SORT,** il sistema invia messaggi [**WM \_ COMPAREITEM**](wm-compareitem.md) al proprietario della casella di riepilogo per determinare quale elemento corrisponde alla stringa specificata. In caso contrario, **LB \_ FINDSTRING** tenta di trovare un elemento con un valore long (fornito come parametro *lParam* del messaggio [**LB \_ ADDSTRING**](lb-addstring.md) o [**LB \_ INSERTSTRING)**](lb-insertstring.md) che corrisponde al *parametro lParam.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                                           |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ FINDSTRINGEXACT**](lb-findstringexact.md)
</dt> </dl>

 

 





