---
description: Inviato a un'applicazione quando il sistema operativo sta per modificare l'IME corrente. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: WM_IME_SELECT messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611ff30bac32fbd38c9aef00e459b49f9760d9702c619f7e6e7f55e6e3b10acb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644621"
---
# <a name="wm_ime_select-message"></a>Messaggio SELECT di WM \_ IME \_

Inviato a un'applicazione quando il sistema operativo sta per modificare l'IME corrente. Una finestra riceve questo messaggio tramite la [*relativa funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
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

Indicatore di selezione. Questo parametro specifica **TRUE se** è selezionato l'IME indicato. Il parametro è impostato su **FALSE se** l'IME specificato non è più selezionato.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificatore delle impostazioni locali di input associato all'IME.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione che ha creato una finestra IME deve passare questo messaggio a tale finestra in modo che possa recuperare l'handle di layout di tastiera per l'IME appena selezionato.

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  elabora questo messaggio passando le informazioni alla finestra IME predefinita.

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

 

 
