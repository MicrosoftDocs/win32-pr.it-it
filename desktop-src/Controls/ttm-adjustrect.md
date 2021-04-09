---
title: Messaggio TTM_ADJUSTRECT (COMmctrl. h)
description: Calcola il rettangolo di visualizzazione del testo di un controllo ToolTip dal rettangolo della finestra o dal rettangolo della finestra della descrizione comando necessario per visualizzare un rettangolo di visualizzazione del testo specificato.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- Controlli di Windows Message TTM_ADJUSTRECT
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
ms.openlocfilehash: af89374161d5e3f9d9ab6affc2b3b498a39cbf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964244"
---
# <a name="ttm_adjustrect-message"></a>\_Messaggio TTM ADJUSTRECT

Calcola il rettangolo di visualizzazione del testo di un controllo ToolTip dal rettangolo della finestra o dal rettangolo della finestra della descrizione comando necessario per visualizzare un rettangolo di visualizzazione del testo specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica l'operazione da eseguire. Se **true**, *lParam* viene usato per specificare un rettangolo di visualizzazione del testo e riceve il rettangolo della finestra corrispondente. Se **false**, *lParam* viene usato per specificare un rettangolo della finestra e riceve il rettangolo di visualizzazione del testo corrispondente.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura **Rect** per mantenere un rettangolo della finestra della descrizione comando o un rettangolo di visualizzazione del testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se il rettangolo viene regolato correttamente e restituisce zero se si verifica un errore.

## <a name="remarks"></a>Commenti

Questo messaggio è particolarmente utile quando si desidera utilizzare un controllo ToolTip per visualizzare il testo completo di una stringa che in genere viene troncata. Viene comunemente usato con i controlli ListView e TreeView. Questo messaggio viene in genere inviato in risposta a un codice di notifica [TTN \_ show](ttn-show.md) per poter posizionare correttamente il controllo ToolTip.

Il rettangolo della finestra della descrizione comando è leggermente più grande del rettangolo di visualizzazione del testo che delimita la stringa della descrizione comando. Anche l'origine della finestra viene spostata verso l'alto e verso sinistra dall'origine del rettangolo di visualizzazione del testo. Per posizionare il rettangolo di visualizzazione del testo, è necessario calcolare il rettangolo della finestra corrispondente e utilizzare tale rettangolo per posizionare la descrizione comando. **TTM \_ ADJUSTRECT** gestisce automaticamente questo calcolo.

Se si imposta *wParam* su **true**, **TTM \_ ADJUSTRECT** acquisisce le dimensioni e la posizione del rettangolo di visualizzazione del testo della descrizione comando desiderato e passa di nuovo le dimensioni e la posizione della finestra della descrizione comando necessaria per visualizzare il testo nella posizione specificata. Se si imposta *wParam* su **false**, è possibile specificare un rettangolo della finestra della descrizione comando e **TTM \_ ADJUSTRECT** restituirà le dimensioni e la posizione del rettangolo di testo.

Il frammento di codice seguente illustra l'uso del messaggio **TTM \_ ADJUSTRECT** per posizionare un controllo ToolTip per visualizzare il testo completo della stringa di un controllo al posto di una stringa troncata. La funzione **GetMyItemRect** definita dall'applicazione restituisce il rettangolo di testo che sarà necessario per visualizzare il testo della descrizione comando direttamente sulla stringa troncata. I dettagli relativi all'implementazione di questa funzione dipenderanno dal particolare controllo. **TTM \_ ADJUSTRECT** viene usato per inviare questo rettangolo di testo al controllo ToolTip. Restituisce un rettangolo della finestra posizionata e dimensionato in modo appropriato che viene quindi usato per posizionare la finestra della descrizione comando.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





