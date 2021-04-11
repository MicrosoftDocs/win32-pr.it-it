---
title: Messaggio WM_CTLCOLORLISTBOX (winuser. h)
description: Inviato alla finestra padre di una casella di riepilogo prima che il sistema disegni la casella di riepilogo. Rispondendo a questo messaggio, la finestra padre può impostare il testo e i colori di sfondo della casella di riepilogo usando l'handle del contesto del dispositivo di visualizzazione specificato.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- Controlli di Windows Message WM_CTLCOLORLISTBOX
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
ms.openlocfilehash: 8e949af76bd05aa9ad3a3e720c89be33cfe76ed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119654"
---
# <a name="wm_ctlcolorlistbox-message"></a>\_Messaggio CTLCOLORLISTBOX WM

Inviato alla finestra padre di una casella di riepilogo prima che il sistema disegni la casella di riepilogo. Rispondendo a questo messaggio, la finestra padre può impostare il testo e i colori di sfondo della casella di riepilogo usando l'handle del contesto del dispositivo di visualizzazione specificato.


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo per la casella di riepilogo.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella di riepilogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire un handle a un pennello. Il sistema utilizza il pennello per disegnare lo sfondo della casella di riepilogo.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per la casella di riepilogo.

Il messaggio **WM \_ CTLCOLORLISTBOX** non viene mai inviato tra i thread. Viene inviato solo all'interno di un thread.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **\_ ptr int** e restituire direttamente il valore. Se la routine della finestra di dialogo restituisce **false**, viene eseguita la gestione dei messaggi predefinita. Il valore **DWL \_ MSGRESULT** impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

