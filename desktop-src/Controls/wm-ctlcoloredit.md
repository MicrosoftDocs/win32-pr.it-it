---
title: WM_CTLCOLOREDIT messaggio (Winuser.h)
description: Un controllo di modifica non di sola lettura o disabilitato invia il messaggio WM CTLCOLOREDIT alla finestra padre quando il controllo \_ sta per essere disegnato.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- WM_CTLCOLOREDIT di controllo Windows messaggio
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
ms.openlocfilehash: da7f1fd27c51cabc699cf945fd4701c36d2e9709d1654de45859777333b9b4bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053901"
---
# <a name="wm_ctlcoloredit-message"></a>Messaggio WM \_ CTLCOLOREDIT

Un controllo di modifica non di sola lettura o disabilitato invia il messaggio **WM \_ CTLCOLOREDIT** alla finestra padre quando il controllo sta per essere disegnato. Rispondendo a questo messaggio, la finestra padre può usare l'handle del contesto di dispositivo specificato per impostare i colori del testo e dello sfondo del controllo di modifica.


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo per la finestra del controllo di modifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo di modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire l'handle di un pennello. Il sistema usa il pennello per disegnare lo sfondo del controllo di modifica.

## <a name="remarks"></a>Commenti

Se l'applicazione restituisce un pennello creato(ad esempio, usando la [**funzione CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect),**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) l'applicazione deve liberare il pennello. Se l'applicazione restituisce un pennello di sistema(ad esempio, uno recuperato dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush),**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) l'applicazione non deve liberare il pennello.

Per impostazione predefinita, la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per il controllo di modifica.

I controlli di modifica di sola lettura o disabilitati non inviano il messaggio **WM \_ CTLCOLOREDIT,** ma inviano il [**messaggio WM \_ CTLCOLORSTATIC.**](wm-ctlcolorstatic.md)

Il **messaggio WM \_ CTLCOLOREDIT** non viene mai inviato tra thread, ma solo all'interno dello stesso thread.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a **un INT \_ PTR** e restituire direttamente il valore. Se la routine della finestra di dialogo restituisce **FALSE,** viene eseguita la gestione dei messaggi predefinita. Il valore MSGRESULT DWL \_ impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

**Rich Edit:** Questo messaggio non è supportato. Per impostare il colore di sfondo per un controllo Rich Edit, usare il messaggio [**EM \_ SETBKGNDCOLOR.**](em-setbkgndcolor.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ SETBKGNDCOLOR**](em-setbkgndcolor.md)
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
</dt> </dl>

 

