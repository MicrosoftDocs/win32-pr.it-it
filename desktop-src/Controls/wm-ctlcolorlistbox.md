---
title: WM_CTLCOLORLISTBOX messaggio (Winuser.h)
description: Inviato alla finestra padre di una casella di riepilogo prima che il sistema disegni la casella di riepilogo. Rispondendo a questo messaggio, la finestra padre può impostare i colori del testo e dello sfondo della casella di riepilogo usando l'handle del contesto di dispositivo di visualizzazione specificato.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- WM_CTLCOLORLISTBOX di controllo Windows messaggio
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1713c7251dfe837d5796b708fa5b77f0aa5e372c031c251199cb871dbd7c5608
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077665"
---
# <a name="wm_ctlcolorlistbox-message"></a>Messaggio \_ WM CTLCOLORLISTBOX

Inviato alla finestra padre di una casella di riepilogo prima che il sistema disegni la casella di riepilogo. Rispondendo a questo messaggio, la finestra padre può impostare i colori del testo e dello sfondo della casella di riepilogo usando l'handle del contesto di dispositivo di visualizzazione specificato.


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle al contesto di dispositivo per la casella di riepilogo.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella di riepilogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire un handle a un pennello. Il sistema usa il pennello per disegnare lo sfondo della casella di riepilogo.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per la casella di riepilogo.

Il **messaggio WM \_ CTLCOLORLISTBOX** non viene mai inviato tra i thread. Viene inviato solo all'interno di un thread.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a **un \_ INT PTR** e restituire direttamente il valore. Se la routine della finestra di dialogo restituisce **FALSE,** viene eseguita la gestione dei messaggi predefinita. Il **valore \_ MSGRESULT DWL** impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelezionarePalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

