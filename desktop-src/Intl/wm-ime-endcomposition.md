---
description: Inviato a un'applicazione quando l'IME termina la composizione. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: WM_IME_ENDCOMPOSITION messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9e19bcf1834d4f9e721efb2a2be53ca20268c7be42109975a7dea52e75d214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560401"
---
# <a name="wm_ime_endcomposition-message"></a>Messaggio \_ ENDCOMPOSITION di WM IME \_

Inviato a un'applicazione quando l'IME termina la composizione. Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,      
  WM_IME_ENDCOMPOSITION,  
  WPARAM wParam,      
  LPARAM lParam             
);
```



## <a name="parameters"></a>Parametri

Questo messaggio non ha parametri.

<dl></dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione deve elaborare questo messaggio se visualizza i caratteri di composizione.

Se l'applicazione ha creato una finestra IME, deve passare questo messaggio a tale finestra. La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  elabora questo messaggio passandolo alla finestra IME predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodi di input](input-method-manager.md)
</dt> <dt>

[Messaggi di Gestione metodo di input](input-method-manager-messages.md)
</dt> </dl>

 

 
