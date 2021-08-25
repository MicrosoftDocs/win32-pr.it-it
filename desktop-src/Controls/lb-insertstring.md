---
title: LB_INSERTSTRING messaggio (Winuser.h)
description: Inserisce i dati di una stringa o di un elemento in una casella di riepilogo. A differenza del messaggio LB ADDSTRING, il messaggio LB INSERTSTRING non determina l'ordinamento di un elenco con lo stile \_ \_ \_ LBS SORT.
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- LB_INSERTSTRING dei messaggi Windows controllo
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
ms.openlocfilehash: dd47d08ef78c590ecb3b5900143b29bc49676b86d8facdcc91b05bb34c8f4aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085391"
---
# <a name="lb_insertstring-message"></a>Messaggio \_ INSERTSTRING LB

Inserisce i dati di una stringa o di un elemento in una casella di riepilogo. A differenza [**del messaggio \_ LB ADDSTRING,**](lb-addstring.md) il messaggio **\_ LB INSERTSTRING** non determina l'ordinamento di un elenco con lo stile [**\_ LBS SORT.**](list-box-styles.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della posizione in corrispondenza della quale inserire la stringa. Se questo parametro è -1, la stringa viene aggiunta alla fine dell'elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione Null da inserire. Se la casella di riepilogo ha uno stile disegnato dal proprietario ma non lo stile [**\_ LBS HASSTRINGS,**](list-box-styles.md) questo parametro viene archiviato come dati dell'elemento anziché come stringa. È possibile inviare [**i messaggi \_ LB GETITEMDATA**](lb-getitemdata.md) e [**LB \_ SETITEMDATA**](lb-setitemdata.md) per recuperare o modificare i dati dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice della posizione in cui è stata inserita la stringa. Se si verifica un errore, il valore restituito è LB \_ ERR. Se lo spazio non è sufficiente per archiviare la nuova stringa, il valore restituito è LB \_ ERRSPACE.

## <a name="remarks"></a>Commenti

Il [**messaggio \_ LB INITSTORAGE**](lb-initstorage.md) consente di velocizzare l'inizializzazione delle caselle di riepilogo con un numero elevato di elementi (più di 100). Riserva la quantità di memoria specificata in modo che i messaggi **\_ INSERTSTRING LB** successivi prendano il tempo più breve possibile. È possibile usare stime per i *parametri wParam* *e lParam.* Se si sovrastima, la memoria aggiuntiva viene allocata; Se si sottovaluta, viene usata l'allocazione normale per gli elementi che superano l'importo richiesto.

Se la casella di riepilogo ha lo stile [**\_ WS HSCROLL**](/windows/desktop/winmsg/window-styles) e si inserisce una stringa più ampia della casella di riepilogo, inviare un [**messaggio LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) per assicurarsi che venga visualizzata la barra di scorrimento orizzontale.

Per un'applicazione ANSI, il sistema converte il testo di una casella di riepilogo in Unicode usando CP \_ ACP. Ciò può causare problemi. Ad esempio, i caratteri romani accentati in una casella di riepilogo non Unicode in lingua Windows verranno visualizzati in gran numero. Per risolvere questo problema, compilare l'applicazione come Unicode o usare una casella di riepilogo disegnata dal proprietario.

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ SELECTSTRING**](lb-selectstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> </dl>

 

