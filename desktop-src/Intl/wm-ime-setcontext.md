---
description: Inviato a un'applicazione quando viene attivata una finestra. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: Messaggio WM_IME_SETCONTEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b36cb1e80127d1a451dabcc457dc364a27878ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226129"
---
# <a name="wm_ime_setcontext-message"></a>Messaggio di contesto di WM \_ IME \_

Inviato a un'applicazione quando viene attivata una finestra. Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
  WPARAM wParam,      
  LPARAM lParam      
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*wParam* 
</dt> <dd>

**True** se la finestra è attiva e **false** in caso contrario.

</dd> <dt>

*lParam* 
</dt> <dd>

Opzioni di visualizzazione. Questo parametro può avere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                   | Significato                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <dt>**\_SHOWUICOMPOSITIONWINDOW ISC**</dt> </dl> | Mostra la finestra di composizione per interfaccia utente.<br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <dt>**\_SHOWUIGUIDWINDOW ISC**</dt> </dl>                      | Mostra la finestra della Guida in base all'interfaccia utente.<br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <dt>**\_SHOWUISOFTKBD ISC**</dt> </dl>                               | Mostra la finestra dell'interfaccia utente della tastiera soft.<br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <dt>**\_SHOWUICANDIDATEWINDOW ISC**</dt> </dl>       | Mostra la finestra candidata dell'indice 0 dalla finestra dell'interfaccia utente.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 1</dt> </dl>                                                                                        | Mostra la finestra candidata di index 1 dalla finestra dell'interfaccia utente.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 2</dt> </dl>                                                                                        | Mostra la finestra candidata di index 2 dalla finestra dell'interfaccia utente.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 3</dt> </dl>                                                                                        | Mostra la finestra candidata di index 3 dalla finestra dell'interfaccia utente.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore restituito da [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).

## <a name="remarks"></a>Commenti

Se l'applicazione ha creato una finestra IME, deve chiamare [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). In caso contrario, deve passare questo messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Se tramite l'applicazione viene disegnata la finestra di composizione, non è necessario che venga visualizzata la finestra di composizione predefinita della finestra IME. In questo caso, l'applicazione deve cancellare il **valore \_ SHOWUICOMPOSITIONWINDOW di ISC** dal *parametro lParam* prima di passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). Per visualizzare una determinata finestra dell'interfaccia utente, un'applicazione deve rimuovere il valore corrispondente in modo che non venga visualizzato dall'IME.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                                                      |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h); </dt> <dt>Imm. h (Includi Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodo di input](input-method-manager.md)
</dt> <dt>

[Messaggi di gestione metodo di input](input-method-manager-messages.md)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
