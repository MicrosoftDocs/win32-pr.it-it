---
description: Inviato a un'applicazione quando viene attivata una finestra. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: WM_IME_SETCONTEXT messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fb3e65b47b5d62b1d37ffaee4dfc5927d76485d0c3e5de02662da64215e43f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829251"
---
# <a name="wm_ime_setcontext-message"></a>Messaggio WM \_ IME \_ SETCONTEXT

Inviato a un'applicazione quando viene attivata una finestra. Una finestra riceve questo messaggio tramite la relativa [*funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*Hwnd* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*wParam* 
</dt> <dd>

**TRUE** se la finestra è attiva e FALSE in **caso contrario.**

</dd> <dt>

*lParam* 
</dt> <dd>

Opzioni di visualizzazione. Questo parametro può avere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                   | Significato                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <dt>**ISC \_ SHOWUICOMPOSITIONWINDOW**</dt> </dl> | Visualizzare la finestra di composizione in base alla finestra dell'interfaccia utente.<br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <dt>**ISC \_ SHOWUIGUIDWINDOW**</dt> </dl>                      | Visualizzare la finestra della guida in base alla finestra dell'interfaccia utente.<br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <dt>**ISC \_ SHOWUISOFTKBD**</dt> </dl>                               | Visualizzare la tastiera soft in base alla finestra dell'interfaccia utente.<br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <dt>**ISC \_ SHOWUICANDIDATEWINDOW**</dt> </dl>       | Visualizzare la finestra candidata dell'indice 0 per finestra dell'interfaccia utente.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 1</dt> </dl>                                                                                        | Visualizzare la finestra candidata dell'indice 1 per finestra dell'interfaccia utente.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 2</dt> </dl>                                                                                        | Visualizzare la finestra candidata dell'indice 2 per finestra dell'interfaccia utente.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 3</dt> </dl>                                                                                        | Visualizzare la finestra candidata dell'indice 3 per finestra dell'interfaccia utente.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore restituito [**da DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage.**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)

## <a name="remarks"></a>Commenti

Se l'applicazione ha creato una finestra IME, deve chiamare [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). In caso contrario, deve passare questo messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Se l'applicazione disegna la finestra di composizione, la finestra IME predefinita non deve visualizzare la finestra di composizione. In questo caso, l'applicazione deve cancellare il valore **ISC \_ SHOWUICOMPOSITIONWINDOW** dal *parametro lParam* prima di passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage.**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) Per visualizzare una determinata finestra dell'interfaccia utente, un'applicazione deve rimuovere il valore corrispondente in modo che l'IME non lo visualizza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                                                      |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h);</dt> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodi di input](input-method-manager.md)
</dt> <dt>

[Messaggi di Gestione metodi di input](input-method-manager-messages.md)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
