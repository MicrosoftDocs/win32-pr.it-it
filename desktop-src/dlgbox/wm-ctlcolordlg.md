---
title: WM_CTLCOLORDLG messaggio (Winuser.h)
description: Inviato a una finestra di dialogo prima che il sistema disegni la finestra di dialogo. Rispondendo a questo messaggio, la finestra di dialogo può impostare i colori del testo e dello sfondo usando l'handle del contesto di dispositivo di visualizzazione specificato.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- WM_CTLCOLORDLG finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b7ab11bbb2cfd402888f930d5bcf2afa08b7ba83f74252fb3e443fd9e9309a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503414"
---
# <a name="wm_ctlcolordlg-message"></a>Messaggio WM \_ CTLCOLORDLG

Inviato a una finestra di dialogo prima che il sistema disegni la finestra di dialogo. Rispondendo a questo messaggio, la finestra di dialogo può impostare i colori del testo e dello sfondo usando l'handle del contesto di dispositivo di visualizzazione specificato.


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo per la finestra di dialogo.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire un handle a un pennello. Il sistema usa il pennello per disegnare lo sfondo della finestra di dialogo.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, [**la funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per la finestra di dialogo.

Il sistema non elimina automaticamente il pennello restituito. È responsabilità dell'applicazione eliminare il pennello quando non è più necessario.

Il **messaggio WM \_ CTLCOLORDLG** non viene mai inviato tra i thread. Viene inviato solo all'interno di un thread.

Si noti che il messaggio **WM \_ CTLCOLORDLG** viene inviato alla finestra di dialogo stessa. Tutti gli altri messaggi **WM \_ CTLCOLOR \*** vengono inviati al proprietario del controllo.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a **un \_ INT PTR** e restituire direttamente il valore. Se la routine della finestra di dialogo restituisce **FALSE,** viene eseguita la gestione dei messaggi predefinita. Il **valore \_ MSGRESULT DWL** impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Setwindowlong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelezionarePalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

