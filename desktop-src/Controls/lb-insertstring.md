---
title: Messaggio LB_INSERTSTRING (winuser. h)
description: Inserisce i dati di una stringa o di un elemento in una casella di riepilogo. A differenza del \_ messaggio lb ADDSTRING, il \_ messaggio lb INSERTSTRING non determina l'ordinamento di un elenco con lo \_ stile di ordinamento lbs.
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- Controlli di Windows Message LB_INSERTSTRING
topic_type:
- apiref
api_name:
- LB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5858af0e0229f90a5ed9928e7478d0ac9a71c8f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121014"
---
# <a name="lb_insertstring-message"></a>\_Messaggio INSERTSTRING lb

Inserisce i dati di una stringa o di un elemento in una casella di riepilogo. A differenza del messaggio [**lb \_ ADDSTRING**](lb-addstring.md) , il messaggio **lb \_ INSERTSTRING** non determina l'ordinamento di un elenco con lo stile di [**\_ ordinamento lbs**](list-box-styles.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della posizione in corrispondenza della quale inserire la stringa. Se questo parametro è-1, la stringa viene aggiunta alla fine dell'elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione null da inserire. Se la casella di riepilogo ha uno stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , questo parametro viene archiviato come dati di elemento anziché come stringa. È possibile inviare i messaggi [**lb \_ GETITEMDATA**](lb-getitemdata.md) e [**lb \_ SETITEMDATA**](lb-setitemdata.md) per recuperare o modificare i dati dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice della posizione in cui è stata inserita la stringa. Se si verifica un errore, il valore restituito è LB \_ Err. Se non è disponibile spazio sufficiente per archiviare la nuova stringa, il valore restituito è LB \_ ERRSPACE.

## <a name="remarks"></a>Commenti

Il messaggio [**lb \_ INITSTORAGE**](lb-initstorage.md) consente di velocizzare l'inizializzazione di caselle di riepilogo con un numero elevato di elementi (più di 100). Si riserva la quantità di memoria specificata in modo che i messaggi **lb \_ INSERTSTRING** il tempo più breve possibile. È possibile utilizzare le stime per i parametri *wParam* e *lParam* . Se si esegue la sovrastima, viene allocata la memoria aggiuntiva. Se si sottovaluta, l'allocazione normale viene utilizzata per gli elementi che superano la quantità richiesta.

Se nella casella di riepilogo è presente lo stile [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e si inserisce una stringa più ampia della casella di riepilogo, inviare un messaggio [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) per assicurarsi che venga visualizzata la barra di scorrimento orizzontale.

Per un'applicazione ANSI, il sistema converte il testo in una casella di riepilogo in formato Unicode usando CP \_ ACP. Ciò può causare problemi. Ad esempio, i caratteri romani accentati in una casella di riepilogo non Unicode nelle finestre giapponesi verranno disattivati. Per risolvere questo problema, compilare l'applicazione come Unicode o utilizzare una casella di riepilogo creata dal proprietario.

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

[**\_ADDSTRING lb**](lb-addstring.md)
</dt> <dt>

[**\_SELECTSTRING lb**](lb-selectstring.md)
</dt> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> </dl>

 

