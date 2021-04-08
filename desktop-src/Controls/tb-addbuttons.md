---
title: Messaggio TB_ADDBUTTONS (COMmctrl. h)
description: Aggiunge uno o più pulsanti a una barra degli strumenti.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- Controlli di Windows Message TB_ADDBUTTONS
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
ms.openlocfilehash: 1f954e9a133f78a9415358d1c7f61d68008cd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965006"
---
# <a name="tb_addbuttons-message"></a>TB \_ ADDBUTTONS messaggio

Aggiunge uno o più pulsanti a una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di pulsanti da aggiungere.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di strutture [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) che contengono informazioni sui pulsanti da aggiungere. Il numero di elementi nella matrice deve essere uguale a quello dei pulsanti specificati da *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Se la barra degli strumenti è stata creata utilizzando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , è necessario inviare il messaggio [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) alla barra degli strumenti prima di inviare **TB \_ ADDBUTTONS**.

Per una discussione su come assegnare bitmap ai pulsanti della barra degli strumenti da uno o più elenchi di immagini, vedere [**TB \_ seimagine**](tb-setimagelist.md) .

## <a name="examples"></a>Esempio

Il codice di esempio seguente aggiunge tre pulsanti a una barra degli strumenti, usando la bitmap di sistema standard per i pulsanti di visualizzazione. Il messaggio [**TB \_ ADDBITMAP**](tb-addbitmap.md) restituisce l'indice della prima immagine del pulsante all'interno dell'elenco di immagini. Le singole immagini vengono identificate in base ai relativi offset da tale valore.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ ADDBUTTONSW** (Unicode) e **TB \_ ADDBUTTONSA** (ANSI)<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Valori di indice dell'immagine del pulsante standard della barra degli strumenti**](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

