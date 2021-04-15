---
title: Messaggio CB_INSERTSTRING (winuser. h)
description: Inserisce i dati di una stringa o di un elemento nell'elenco di una casella combinata. A differenza del \_ messaggio CB ADDSTRING, il \_ messaggio CB INSERTSTRING non determina l'ordinamento di un elenco con lo \_ stile di ordinamento CBS.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- Controlli di Windows Message CB_INSERTSTRING
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
ms.openlocfilehash: 14d050980137bc34652cb2fce39b9f188f4d5cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476649"
---
# <a name="cb_insertstring-message"></a>\_Messaggio INSERTSTRING CB

Inserisce i dati di una stringa o di un elemento nell'elenco di una casella combinata. A differenza del messaggio [**CB \_ ADDSTRING**](cb-addstring.md) , il messaggio **CB \_ INSERTSTRING** non determina l'ordinamento di un elenco con lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della posizione in corrispondenza della quale inserire la stringa. Se questo parametro è-1, la stringa viene aggiunta alla fine dell'elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione null da inserire. Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo [**stile \_ HASSTRINGS CBS**](combo-box-styles.md) , il valore del parametro *lParam* viene archiviato anziché la stringa a cui altrimenti indicherà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice della posizione in cui è stata inserita la stringa. Se si verifica un errore, il valore restituito è CB \_ Err. Se non è disponibile spazio sufficiente per archiviare la nuova stringa, è CB \_ ERRSPACE.

Se lo stile della casella combinata è [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e si inserisce una stringa più ampia della casella combinata, è necessario inviare un messaggio [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) per assicurarsi che venga visualizzata la barra di scorrimento orizzontale.

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

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> <dt>

[**DIR della CB \_**](cb-dir.md)
</dt> </dl>

 

