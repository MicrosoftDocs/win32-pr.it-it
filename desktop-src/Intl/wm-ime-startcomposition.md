---
description: Inviato immediatamente prima che l'IME generi la stringa di composizione come risultato di una sequenza di tasti. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 2740d009-8685-4f70-9b01-67b71f4ddcbd
title: Messaggio WM_IME_STARTCOMPOSITION (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bd9a93b4c6c2e8dba6658c84b5f431dd9a54e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879290"
---
# <a name="wm_ime_startcomposition-message"></a>\_ \_ Messaggio STARTCOMPOSITION di WM IME

Inviato immediatamente prima che l'IME generi la stringa di composizione come risultato di una sequenza di tasti. Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,                
  WM_IME_STARTCOMPOSITION,  
  WPARAM wParam,            
  LPARAM lParam             
);
```



## <a name="parameters"></a>Parametri

Questo messaggio non contiene parametri.

<dl></dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Questo messaggio è una notifica a una finestra IME per aprire la relativa finestra di composizione. Un'applicazione deve elaborare questo messaggio se Visualizza caratteri di composizione.

Se un'applicazione ha creato una finestra IME, deve passare questo messaggio a tale finestra. La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) elabora il messaggio passandolo alla finestra IME predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodo di input](input-method-manager.md)
</dt> <dt>

[Messaggi di gestione metodo di input](input-method-manager-messages.md)
</dt> </dl>

 

 
