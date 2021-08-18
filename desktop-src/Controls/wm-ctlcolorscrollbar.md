---
title: WM_CTLCOLORSCROLLBAR messaggio (Winuser.h)
description: Il messaggio WM CTLCOLORSCROLLBAR viene inviato alla finestra padre di un controllo barra di scorrimento quando il controllo sta \_ per essere disegnato.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- WM_CTLCOLORSCROLLBAR del messaggio Windows controlli
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35dba3394c3d8fd99fef88d6fa1869ea1129d95ae8a82cc33f2935e5688871a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018559"
---
# <a name="wm_ctlcolorscrollbar-message"></a>Messaggio DI WM \_ CTLCOLORSCROLLBAR

Il **messaggio WM \_ CTLCOLORSCROLLBAR** viene inviato alla finestra padre di un controllo barra di scorrimento quando il controllo sta per essere disegnato. Rispondendo a questo messaggio, la finestra padre può usare l'handle del contesto di visualizzazione per impostare il colore di sfondo del controllo barra di scorrimento.

Una finestra riceve questo messaggio tramite la [*relativa funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo per il controllo barra di scorrimento.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la barra di scorrimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire l'handle a un pennello. Il sistema usa il pennello per disegnare lo sfondo del controllo barra di scorrimento.

## <a name="remarks"></a>Commenti

Se l'applicazione restituisce un pennello creato ,ad esempio usando la funzione [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect,**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) l'applicazione deve liberare il pennello. Se l'applicazione restituisce un pennello di sistema,ad esempio un pennello recuperato dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush,**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) non è necessario liberare il pennello.

Per impostazione predefinita, la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per il controllo barra di scorrimento.

Il **messaggio WM \_ CTLCOLORSCROLLBAR** non viene mai inviato tra thread, ma solo all'interno dello stesso thread.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a **un \_ int PTR** e restituire direttamente il valore. Se la routine della finestra di dialogo **restituisce FALSE,** viene eseguita la gestione dei messaggi predefinita. Il valore MSGRESULT DWL \_ impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

Il **messaggio WM \_ CTLCOLORSCROLLBAR** viene usato solo dai controlli barra di scorrimento figlio. Le barre di scorrimento associate a una finestra (WS \_ SCROLL e WS \_ VSCROLL) non generano questo messaggio. Per personalizzare l'aspetto delle barre di scorrimento associate a una finestra, usare le funzioni della barra di scorrimento flat.

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

[**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md)
</dt> <dt>

[**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md)
</dt> <dt>

[**WM \_ CTLCOLORLISTBOX**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelezionarePalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**WM \_ CTLCOLORDLG**](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

