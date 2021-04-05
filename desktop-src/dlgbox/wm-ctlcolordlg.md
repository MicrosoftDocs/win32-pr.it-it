---
title: Messaggio WM_CTLCOLORDLG (winuser. h)
description: Inviato a una finestra di dialogo prima che il sistema disegni la finestra di dialogo. Rispondendo a questo messaggio, la finestra di dialogo può impostare il testo e i colori di sfondo usando l'handle del contesto del dispositivo di visualizzazione specificato.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- Finestre di dialogo WM_CTLCOLORDLG messaggio
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
ms.openlocfilehash: 833d3894a85342b0f26323ceed0f4fb3356c48ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740154"
---
# <a name="wm_ctlcolordlg-message"></a>\_Messaggio CTLCOLORDLG WM

Inviato a una finestra di dialogo prima che il sistema disegni la finestra di dialogo. Rispondendo a questo messaggio, la finestra di dialogo può impostare il testo e i colori di sfondo usando l'handle del contesto del dispositivo di visualizzazione specificato.


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

Se un'applicazione elabora il messaggio, deve restituire un handle a un pennello. Il sistema utilizza il pennello per disegnare lo sfondo della finestra di dialogo.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per la finestra di dialogo.

Il sistema non elimina automaticamente il pennello restituito. È responsabilità dell'applicazione eliminare il pennello quando non è più necessario.

Il messaggio **WM \_ CTLCOLORDLG** non viene mai inviato tra i thread. Viene inviato solo all'interno di un thread.

Si noti che il messaggio **WM \_ CTLCOLORDLG** viene inviato alla finestra di dialogo; tutti gli altri **WM \_ CTLCOLOR \** _ messaggi vengono inviati al proprietario del controllo.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un _ *int \_ ptr** e restituire direttamente il valore. Se la routine della finestra di dialogo restituisce **false**, viene eseguita la gestione dei messaggi predefinita. Il valore **DWL \_ MSGRESULT** impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

