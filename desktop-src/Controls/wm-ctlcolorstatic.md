---
title: Messaggio WM_CTLCOLORSTATIC (winuser. h)
description: Un controllo statico o un controllo di modifica che è di sola lettura o disabilitato invia il \_ messaggio CTLCOLORSTATIC WM alla relativa finestra padre quando il controllo sta per essere disegnato.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- Controlli di Windows Message WM_CTLCOLORSTATIC
topic_type:
- apiref
api_name:
- WM_CTLCOLORSTATIC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851879eeb65a00f95f8cb81cef1b6c23ece8028d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741367"
---
# <a name="wm_ctlcolorstatic-message"></a>\_Messaggio CTLCOLORSTATIC WM

Un controllo statico o un controllo di modifica che è di sola lettura o disabilitato invia il **messaggio \_ CTLCOLORSTATIC WM** alla relativa finestra padre quando il controllo sta per essere disegnato. Rispondendo a questo messaggio, la finestra padre può usare l'handle del contesto di dispositivo specificato per impostare i colori di primo piano e di sfondo del testo del controllo statico.

Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo per la finestra del controllo statico.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo statico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, il valore restituito è un handle per un pennello utilizzato dal sistema per disegnare lo sfondo del controllo statico.

## <a name="remarks"></a>Commenti

Se l'applicazione restituisce un pennello creato, ad esempio tramite la funzione [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) , l'applicazione deve liberare il pennello. Se l'applicazione restituisce un pennello di sistema, ad esempio uno recuperato dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) , l'applicazione non deve liberare il pennello.

Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per il controllo statico.

È possibile impostare il colore di sfondo del testo di un controllo di modifica disabilitato, ma non è possibile impostare il colore di primo piano del testo. Il sistema usa sempre il colore \_ GRAYTEXT.

I controlli di modifica che non sono di sola lettura o disabilitati non inviano il messaggio **WM \_ CTLCOLORSTATIC** , bensì inviano il messaggio [**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) .

Il messaggio **WM \_ CTLCOLORSTATIC** non viene mai inviato tra i thread, ma viene inviato solo all'interno dello stesso thread.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **\_ ptr int** e restituire direttamente il valore. Se la routine della finestra di dialogo restituisce **false**, viene eseguita la gestione dei messaggi predefinita. Il \_ valore DWL MSGRESULT impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

## <a name="examples"></a>Esempio

Nell'esempio C++ riportato di seguito viene illustrato come impostare i colori di primo piano e di sfondo del testo di un controllo statico in risposta al messaggio **WM \_ CTLCOLORSTATIC** . La `hbrBkgnd` variabile è una variabile **HBRUSH** statica inizializzata su null e archivia il pennello di sfondo tra le chiamate a **WM \_ CTLCOLORSTATIC**. Il pennello deve essere eliminato da una chiamata alla funzione [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) quando non è più necessario, in genere quando la finestra di dialogo associata viene distrutta.


```C++
   case WM_CTLCOLORSTATIC:
        {
        HDC hdcStatic = (HDC) wParam;
        SetTextColor(hdcStatic, RGB(255,255,255));
        SetBkColor(hdcStatic, RGB(0,0,0));

        if (hbrBkgnd == NULL)
        {
            hbrBkgnd = CreateSolidBrush(RGB(0,0,0));
        }
        return (INT_PTR)hbrBkgnd;
        }
```



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

[**\_CTLCOLORSCROLLBAR WM**](wm-ctlcolorscrollbar.md)
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

 

