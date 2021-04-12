---
description: Inviato a un'applicazione quando la finestra IME non trova alcuno spazio per estendere l'area per la finestra di composizione. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: Messaggio WM_IME_COMPOSITIONFULL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33051ac3e4e893eb803d4b13d7bfbf53751258b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234187"
---
# <a name="wm_ime_compositionfull-message"></a>\_ \_ Messaggio COMPOSITIONFULL di WM IME

Inviato a un'applicazione quando la finestra IME non trova alcuno spazio per estendere l'area per la finestra di composizione. Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
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

L'applicazione deve usare il comando [IMC \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) per specificare la modalità di visualizzazione della finestra.

La finestra IME, anziché l'IME, invia questo messaggio di notifica tramite la funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) .

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
</dt> <dt>

[\_SETCOMPOSITIONWINDOW IMC](imc-setcompositionwindow.md)
</dt> </dl>

 

 
