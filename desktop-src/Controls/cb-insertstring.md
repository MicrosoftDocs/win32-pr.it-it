---
title: CB_INSERTSTRING messaggio (Winuser.h)
description: Inserisce i dati di una stringa o di un elemento nell'elenco di una casella combinata. A differenza del messaggio CB ADDSTRING, il messaggio CB INSERTSTRING non determina l'ordinamento di un elenco con lo stile \_ \_ \_ CBS SORT.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- CB_INSERTSTRING di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcebd3ed5c52a40f3ca5d49031948f76edfa9d6d98974cec104c4b8e283c101a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089071"
---
# <a name="cb_insertstring-message"></a>Messaggio \_ INSERTSTRING CB

Inserisce i dati di una stringa o di un elemento nell'elenco di una casella combinata. A differenza [**del messaggio \_ CB ADDSTRING,**](cb-addstring.md) il messaggio **CB \_ INSERTSTRING** non determina l'ordinamento di un elenco con lo stile [**\_ CBS SORT.**](combo-box-styles.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della posizione in corrispondenza della quale inserire la stringa. Se questo parametro è -1, la stringa viene aggiunta alla fine dell'elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione Null da inserire. Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo stile [**\_ CBS HASSTRINGS,**](combo-box-styles.md) il valore del *parametro lParam* viene archiviato anziché la stringa a cui punta in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice della posizione in cui è stata inserita la stringa. Se si verifica un errore, il valore restituito è CB \_ ERR. Se lo spazio disponibile non è sufficiente per archiviare la nuova stringa, si tratta di CB \_ ERRSPACE.

Se la casella combinata ha lo stile [**\_ WS HSCROLL**](/windows/desktop/winmsg/window-styles) e si inserisce una stringa più ampia della casella combinata, è necessario inviare un messaggio [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) per assicurarsi che venga visualizzata la barra di scorrimento orizzontale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**CB \_ DIR**](cb-dir.md)
</dt> </dl>

 

