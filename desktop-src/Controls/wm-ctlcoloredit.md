---
title: Messaggio WM_CTLCOLOREDIT (winuser. h)
description: Un controllo di modifica che non è di sola lettura o disabilitato invia il \_ messaggio WM CTLCOLOREDIT alla relativa finestra padre quando il controllo sta per essere disegnato.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- Controlli di Windows Message WM_CTLCOLOREDIT
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475112"
---
# <a name="wm_ctlcoloredit-message"></a>\_Messaggio CTLCOLOREDIT WM

Un controllo di modifica che non è di sola lettura o disabilitato invia il messaggio **WM \_ CTLCOLOREDIT** alla relativa finestra padre quando il controllo sta per essere disegnato. Rispondendo a questo messaggio, la finestra padre può usare l'handle del contesto di dispositivo specificato per impostare il testo e i colori di sfondo del controllo di modifica.


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo per la finestra di controllo di modifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo di modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire l'handle di un pennello. Il sistema utilizza il pennello per disegnare lo sfondo del controllo di modifica.

## <a name="remarks"></a>Commenti

Se l'applicazione restituisce un pennello creato, ad esempio tramite la funzione [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) , l'applicazione deve liberare il pennello. Se l'applicazione restituisce un pennello di sistema, ad esempio uno recuperato dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) , l'applicazione non deve liberare il pennello.

Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per il controllo di modifica.

I controlli di modifica di sola lettura o disabilitato non inviano il messaggio **WM \_ CTLCOLOREDIT** , bensì inviano il messaggio [**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) .

Il messaggio **WM \_ CTLCOLOREDIT** non viene mai inviato tra i thread, ma viene inviato solo all'interno dello stesso thread.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **\_ ptr int** e restituire direttamente il valore. Se la routine della finestra di dialogo restituisce **false**, viene eseguita la gestione dei messaggi predefinita. Il \_ valore DWL MSGRESULT impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

**Modifica avanzata:** Questo messaggio non è supportato. Per impostare il colore di sfondo per un controllo Rich Edit, utilizzare il messaggio [**\_ SETBKGNDCOLOR em**](em-setbkgndcolor.md) .

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

[**\_SETBKGNDCOLOR em**](em-setbkgndcolor.md)
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
</dt> </dl>

 

