---
title: Messaggio LB_ADDSTRING (winuser. h)
description: Aggiunge una stringa a una casella di riepilogo. Se la casella di riepilogo non ha lo \_ stile di ordinamento lbs, la stringa viene aggiunta alla fine dell'elenco. In caso contrario, la stringa viene inserita nell'elenco e l'elenco viene ordinato.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- Controlli di Windows Message LB_ADDSTRING
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
ms.openlocfilehash: 87e1c820b7a4c122012076c82ce20adc0d01e2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048297"
---
# <a name="lb_addstring-message"></a>\_Messaggio ADDSTRING lb

Aggiunge una stringa a una casella di riepilogo. Se la casella di riepilogo non ha lo stile di [**\_ ordinamento lbs**](list-box-styles.md) , la stringa viene aggiunta alla fine dell'elenco. In caso contrario, la stringa viene inserita nell'elenco e l'elenco viene ordinato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione null da aggiungere.

Se la casella di riepilogo ha uno stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , questo parametro viene archiviato come dati di elemento anziché come stringa. È possibile inviare i messaggi **lb \_ GETITEMDATA** e **lb \_ SETITEMDATA** per recuperare o modificare i dati dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice in base zero della stringa nella casella di riepilogo. Se si verifica un errore, il valore restituito è LB \_ Err. Se non è disponibile spazio sufficiente per archiviare la nuova stringa, il valore restituito è LB \_ ERRSPACE.

## <a name="remarks"></a>Commenti

Se la casella di riepilogo ha uno stile disegnato dal proprietario e lo stile di [**\_ ordinamento lbs**](list-box-styles.md) , ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , il sistema invia il messaggio [**WM \_ COMPAREITEM**](wm-compareitem.md) una o più volte al proprietario della casella di riepilogo per inserire il nuovo elemento correttamente nella casella di riepilogo.

Il messaggio [**lb \_ INITSTORAGE**](lb-initstorage.md) consente di velocizzare l'inizializzazione di caselle di riepilogo con un numero elevato di elementi (più di 100). Si riserva la quantità di memoria specificata in modo che i messaggi **lb \_ ADDSTRING** il tempo più breve possibile. È possibile utilizzare le stime per i parametri *wParam* e *lParam* . Se si esegue la sovrastima, viene allocata la memoria aggiuntiva. Se si sottovaluta, l'allocazione normale viene utilizzata per gli elementi che superano la quantità richiesta.

Se la casella di riepilogo ha lo stile [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e si aggiunge una stringa più ampia della casella di riepilogo, inviare un messaggio [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) per assicurarsi che venga visualizzata la barra di scorrimento orizzontale.

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

[**\_DELETESTRING lb**](lb-deletestring.md)
</dt> <dt>

[**\_INSERTSTRING lb**](lb-insertstring.md)
</dt> <dt>

[**\_SELECTSTRING lb**](lb-selectstring.md)
</dt> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> <dt>

[**\_COMPAREITEM WM**](wm-compareitem.md)
</dt> </dl>

 

