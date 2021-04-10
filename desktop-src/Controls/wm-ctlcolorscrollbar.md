---
title: Messaggio WM_CTLCOLORSCROLLBAR (winuser. h)
description: Il \_ messaggio WM CTLCOLORSCROLLBAR viene inviato alla finestra padre di un controllo barra di scorrimento quando il controllo sta per essere disegnato.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- Controlli di Windows Message WM_CTLCOLORSCROLLBAR
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
ms.openlocfilehash: a3f8282e8e15bf1d1a668e1f57e17048f0babac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964156"
---
# <a name="wm_ctlcolorscrollbar-message"></a>\_Messaggio CTLCOLORSCROLLBAR WM

Il messaggio **WM \_ CTLCOLORSCROLLBAR** viene inviato alla finestra padre di un controllo barra di scorrimento quando il controllo sta per essere disegnato. Rispondendo a questo messaggio, la finestra padre può utilizzare l'handle del contesto di visualizzazione per impostare il colore di sfondo del controllo barra di scorrimento.

Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

Se un'applicazione elabora il messaggio, deve restituire l'handle a un pennello. Il sistema utilizza il pennello per disegnare lo sfondo del controllo barra di scorrimento.

## <a name="remarks"></a>Commenti

Se l'applicazione restituisce un pennello creato, ad esempio tramite la funzione [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) , l'applicazione deve liberare il pennello. Se l'applicazione restituisce un pennello di sistema, ad esempio uno recuperato dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) , l'applicazione non deve liberare il pennello.

Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per il controllo barra di scorrimento.

Il messaggio **WM \_ CTLCOLORSCROLLBAR** non viene mai inviato tra i thread, ma viene inviato solo all'interno dello stesso thread.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **\_ ptr int** e restituire direttamente il valore. Se la routine della finestra di dialogo restituisce **false**, viene eseguita la gestione dei messaggi predefinita. Il \_ valore DWL MSGRESULT impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

Il messaggio **WM \_ CTLCOLORSCROLLBAR** viene usato solo dai controlli della barra di scorrimento figlio. Le barre di scorrimento associate a una finestra (WS \_ Scroll e WS \_ VSCROLL) non generano questo messaggio. Per personalizzare l'aspetto delle barre di scorrimento associate a una finestra, utilizzare le funzioni della barra di scorrimento flat.

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

[**\_CTLCOLORBTN WM**](wm-ctlcolorbtn.md)
</dt> <dt>

[**\_CTLCOLOREDIT WM**](wm-ctlcoloredit.md)
</dt> <dt>

[**\_CTLCOLORLISTBOX WM**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**\_CTLCOLORSTATIC WM**](wm-ctlcolorstatic.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**\_CTLCOLORDLG WM**](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

