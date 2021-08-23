---
title: TTM_ADJUSTRECT messaggio (Commctrl.h)
description: Calcola il rettangolo di visualizzazione del testo di un controllo descrizione comando dal rettangolo della finestra o il rettangolo della finestra della descrizione comando necessario per visualizzare un rettangolo di visualizzazione del testo specificato.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- TTM_ADJUSTRECT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TTM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba5a6719bcbd820d94b6d736a12644f8b2539cc81064f942616c62bce55823f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769531"
---
# <a name="ttm_adjustrect-message"></a>Messaggio TTM \_ ADJUSTRECT

Calcola il rettangolo di visualizzazione del testo di un controllo descrizione comando dal rettangolo della finestra o il rettangolo della finestra della descrizione comando necessario per visualizzare un rettangolo di visualizzazione del testo specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica l'operazione da eseguire. Se **TRUE,** *lParam* viene usato per specificare un rettangolo di visualizzazione del testo e riceve il rettangolo della finestra corrispondente. Se **FALSE,** *lParam viene* usato per specificare un rettangolo della finestra e riceve il rettangolo di visualizzazione del testo corrispondente.

</dd> <dt>

*lParam* 
</dt> <dd>

**Struttura RECT** per contenere un rettangolo della finestra della descrizione comando o un rettangolo di visualizzazione del testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se il rettangolo viene regolato correttamente e restituisce zero se si verifica un errore.

## <a name="remarks"></a>Commenti

Questo messaggio è particolarmente utile quando si vuole usare un controllo descrizione comando per visualizzare il testo completo di una stringa che in genere viene troncata. Viene comunemente usato con i controlli listview e treeview. Questo messaggio viene in genere inviato in risposta a un codice di notifica [TTN \_ SHOW](ttn-show.md) in modo da poter posizionare correttamente il controllo descrizione comando.

Il rettangolo della finestra della descrizione comando è leggermente più grande del rettangolo di visualizzazione del testo che delimita la stringa della descrizione comando. Anche l'origine della finestra viene compensata verso l'alto e a sinistra rispetto all'origine del rettangolo di visualizzazione del testo. Per posizionare il rettangolo di visualizzazione del testo, è necessario calcolare il rettangolo della finestra corrispondente e usare tale rettangolo per posizionare la descrizione comando. **TTM \_ ADJUSTRECT gestisce** automaticamente questo calcolo.

Se si imposta *wParam* su **TRUE,** **TTM \_ ADJUSTRECT** accetta le dimensioni e la posizione del rettangolo di visualizzazione del testo della descrizione comando desiderato e restituisce le dimensioni e la posizione della finestra della descrizione comando necessaria per visualizzare il testo nella posizione specificata. Se si imposta *wParam* su **FALSE,** è possibile specificare un rettangolo della finestra della descrizione comando e **TTM \_ ADJUSTRECT** restituirà le dimensioni e la posizione del rettangolo di testo.

Il frammento di codice seguente illustra l'uso del messaggio **TTM \_ ADJUSTRECT** per posizionare un controllo descrizione comando per visualizzare il testo completo della stringa di un controllo al posto di una stringa troncata. La funzione **GetMyItemRect** definita dall'applicazione restituisce il rettangolo di testo necessario per visualizzare il testo della descrizione comando direttamente sulla stringa troncata. I dettagli della modalità di implementazione di questa funzione dipendono dal controllo specifico. **TTM \_ ADJUSTRECT viene usato** per inviare questo rettangolo di testo al controllo descrizione comando. Restituisce un rettangolo di finestra posizionato e ridimensionato in modo appropriato che viene quindi usato per posizionare la finestra della descrizione comando.


```
case TTN_SHOW:

if (MyStringIsTruncated) {
    RECT rc;
    
    GetMyItemRect(&rc);
    SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
    SetWindowPos(hwndToolTip,
                 NULL,
                 rc.left, rc.top,
                 0, 0,
                 SWP_NOSIZE|SWP_NOZORDER|SWP_NOACTIVATE);
} 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





