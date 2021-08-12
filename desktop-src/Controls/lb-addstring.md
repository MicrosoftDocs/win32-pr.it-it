---
title: LB_ADDSTRING messaggio (Winuser.h)
description: Aggiunge una stringa a una casella di riepilogo. Se la casella di riepilogo non ha lo stile LBS \_ SORT, la stringa viene aggiunta alla fine dell'elenco. In caso contrario, la stringa viene inserita nell'elenco e l'elenco viene ordinato.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- LB_ADDSTRING di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 552e3c344a730ad1fc00337cafa71a19a6586b9a4c95f2ed1ebce352d9d909aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671687"
---
# <a name="lb_addstring-message"></a>LB \_ ADDSTRING message

Aggiunge una stringa a una casella di riepilogo. Se la casella di riepilogo non ha lo stile [**LBS \_ SORT,**](list-box-styles.md) la stringa viene aggiunta alla fine dell'elenco. In caso contrario, la stringa viene inserita nell'elenco e l'elenco viene ordinato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione Null da aggiungere.

Se la casella di riepilogo ha uno stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS di LBS,**](list-box-styles.md) questo parametro viene archiviato come dati dell'elemento anziché come stringa. È possibile inviare **i messaggi \_ LB GETITEMDATA** e **\_ LB SETITEMDATA** per recuperare o modificare i dati dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice in base zero della stringa nella casella di riepilogo. Se si verifica un errore, il valore restituito è LB \_ ERR. Se lo spazio disponibile non è sufficiente per archiviare la nuova stringa, il valore restituito è LB \_ ERRSPACE.

## <a name="remarks"></a>Commenti

Se la casella di riepilogo ha uno stile creato dal proprietario e lo stile [**LBS \_ SORT,**](list-box-styles.md) ma non lo stile [**\_ HASSTRINGS di LBS,**](list-box-styles.md) il sistema invia il messaggio [**WM \_ COMPAREITEM**](wm-compareitem.md) una o più volte al proprietario della casella di riepilogo per inserire correttamente il nuovo elemento nella casella di riepilogo.

Il [**messaggio \_ LB INITSTORAGE**](lb-initstorage.md) consente di velocizzare l'inizializzazione delle caselle di riepilogo con un numero elevato di elementi (più di 100). Riserva la quantità di memoria specificata in modo che i successivi messaggi **\_ LB ADDSTRING** prendano il tempo più breve possibile. È possibile usare stime per i *parametri wParam* *e lParam.* Se si sovrastima, viene allocata memoria aggiuntiva. Se si sottovaluta, l'allocazione normale viene usata per gli elementi che superano la quantità richiesta.

Se la casella di riepilogo ha lo stile [**\_ WS HSCROLL**](/windows/desktop/winmsg/window-styles) e si aggiunge una stringa più ampia della casella di riepilogo, inviare un messaggio [**\_ LB SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) per assicurarsi che venga visualizzata la barra di scorrimento orizzontale.

Per un'applicazione ANSI, il sistema converte il testo in una casella di riepilogo in Unicode usando CP \_ ACP. Ciò può causare problemi. Ad esempio, i caratteri romani accentati in una casella di riepilogo non Unicode in giapponese Windows verranno visualizzati in gran parte. Per risolvere questo problema, compilare l'applicazione come Unicode o usare una casella di riepilogo disegnata dal proprietario.

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

[**LB \_ DELETESTRING**](lb-deletestring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> <dt>

[**LB \_ SELECTSTRING**](lb-selectstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

