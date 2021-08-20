---
title: TB_ADDBUTTONS messaggio (Commctrl.h)
description: Aggiunge uno o più pulsanti a una barra degli strumenti.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- TB_ADDBUTTONS dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TB_ADDBUTTONS
- TB_ADDBUTTONSA
- TB_ADDBUTTONSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd3a5a15ac1983d93ca161dae20876159e5f633cf580d485686d67889276747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168524"
---
# <a name="tb_addbuttons-message"></a>Tb \_ ADDBUTTONS message

Aggiunge uno o più pulsanti a una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di pulsanti da aggiungere.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di [**strutture TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) che contengono informazioni sui pulsanti da aggiungere. Nella matrice deve essere presente lo stesso numero di elementi dei pulsanti specificati da *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Se la barra degli strumenti è stata creata usando la [**funzione CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) è necessario inviare il messaggio [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) alla barra degli strumenti prima di inviare **TB \_ ADDBUTTONS**.

Per informazioni su come assegnare bitmap ai pulsanti della barra degli strumenti da uno o più elenchi di immagini, vedere [**TB \_ SETIMAGELIST.**](tb-setimagelist.md)

## <a name="examples"></a>Esempio

Il codice di esempio seguente aggiunge tre pulsanti a una barra degli strumenti, usando la bitmap di sistema standard per i pulsanti di visualizzazione. Il [**messaggio \_ TB ADDBITMAP**](tb-addbitmap.md) restituisce l'indice della prima immagine del pulsante all'interno dell'elenco di immagini. Le singole immagini vengono identificate in base ai relativi offset da tale valore.


```C++
TBADDBITMAP tbAddBitmap;
tbAddBitmap.hInst = HINST_COMMCTRL;
tbAddBitmap.nID = IDB_VIEW_SMALL_COLOR;

// There are 12 items in IDB_VIEW_SMALL_COLOR.  However, because this is a standard
// system-defined bitmap, the wParam (nButtons) is ignored.
//
// hWndToolbar is the handle of the toolbar window.
//
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was created
// by using CreateWindowEx.
//
int stdidx = SendMessage(hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tbAddBitmap);

// Define the buttons. 
// IDM_SETLARGEICONVIEW and so on are application-defined command IDs.

const int numButtons = 3;
TBBUTTON tbButtonsAdd[numButtons] = 
{
    {stdidx + VIEW_LARGEICONS, IDM_SETLARGEICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_SMALLICONS, IDM_SETSMALLICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_DETAILS, IDM_SETDETAILSVIEW, TBSTATE_ENABLED, BTNS_BUTTON}
}; 

// Add the view buttons.
SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)tbButtonsAdd);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ ADDBUTTONSW** (Unicode) e **TB \_ ADDBUTTONSA** (ANSI)<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Valori di indice delle immagini dei pulsanti standard della barra degli strumenti**](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

