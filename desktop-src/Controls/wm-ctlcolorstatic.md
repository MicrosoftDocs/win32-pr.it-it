---
title: WM_CTLCOLORSTATIC messaggio (Winuser.h)
description: Un controllo statico o un controllo di modifica di sola lettura o disabilitato invia il messaggio WM CTLCOLORSTATIC alla finestra padre quando il controllo sta \_ per essere disegnato.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- WM_CTLCOLORSTATIC dei controlli Windows messaggio
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
ms.openlocfilehash: 2df23b86539d07c9e1551d64f59e60e54df24ae2d48b316996542fb80c92ae8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539931"
---
# <a name="wm_ctlcolorstatic-message"></a>Messaggio \_ WM CTLCOLORSTATIC

Un controllo statico o un controllo di modifica di sola lettura o disabilitato invia il messaggio **WM \_ CTLCOLORSTATIC** alla finestra padre quando il controllo sta per essere disegnato. Rispondendo a questo messaggio, la finestra padre può usare l'handle del contesto di dispositivo specificato per impostare i colori di primo piano e di sfondo del testo del controllo statico.

Una finestra riceve questo messaggio tramite la [*relativa funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo per la finestra di controllo statica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo statico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, il valore restituito è un handle a un pennello utilizzato dal sistema per disegnare lo sfondo del controllo statico.

## <a name="remarks"></a>Commenti

Se l'applicazione restituisce un pennello creato ,ad esempio usando la funzione [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect,**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) l'applicazione deve liberare il pennello. Se l'applicazione restituisce un pennello di sistema,ad esempio un pennello recuperato dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush,**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) non è necessario liberare il pennello.

Per impostazione predefinita, [**la funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per il controllo statico.

È possibile impostare il colore di sfondo del testo di un controllo di modifica disabilitato, ma non è possibile impostare il colore di primo piano del testo. Il sistema usa sempre COLOR \_ GRAYTEXT.

I controlli di modifica non di sola lettura o disabilitati non inviano il messaggio **WM \_ CTLCOLORSTATIC,** ma inviano il [**messaggio WM \_ CTLCOLOREDIT.**](wm-ctlcoloredit.md)

Il **messaggio WM \_ CTLCOLORSTATIC** non viene mai inviato tra thread, ma solo all'interno dello stesso thread.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a **un \_ int PTR** e restituire direttamente il valore. Se la routine della finestra di dialogo **restituisce FALSE,** viene eseguita la gestione dei messaggi predefinita. Il valore MSGRESULT DWL \_ impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

## <a name="examples"></a>Esempio

Nell'esempio C++ seguente viene illustrato come impostare i colori di primo piano e di sfondo del testo di un controllo statico in risposta al messaggio **WM \_ CTLCOLORSTATIC.** La variabile è una variabile HBRUSH statica inizializzata su NULL e archivia il pennello di sfondo tra le chiamate `hbrBkgnd` a **WM \_ CTLCOLORSTATIC.**  Il pennello deve essere eliminato definitivamente da una chiamata alla funzione [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) quando non è più necessario, in genere quando la finestra di dialogo associata viene distrutta.


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

[**WM \_ CTLCOLORSCROLLBAR**](wm-ctlcolorscrollbar.md)
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

 

