---
description: Inviato a un'applicazione quando la finestra IME non trova spazio per estendere l'area per la finestra di composizione. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: WM_IME_COMPOSITIONFULL messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954a5f91283ca5c4944c274d422508ef0b91b55b8acc34f790cf446f93a598ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811491"
---
# <a name="wm_ime_compositionfull-message"></a>Messaggio WM \_ IME \_ COMPOSITIONFULL

Inviato a un'applicazione quando la finestra IME non trova spazio per estendere l'area per la finestra di composizione. Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
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

L'applicazione deve usare [il comando \_ IMC SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) per specificare la modalità di visualizzazione della finestra.

La finestra IME, anziché l'IME, invia questo messaggio di notifica dalla [**funzione SendMessage.**](/windows/win32/api/winuser/nf-winuser-sendmessage)

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
</dt> <dt>

[IMC \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md)
</dt> </dl>

 

 
