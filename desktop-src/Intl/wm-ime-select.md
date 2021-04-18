---
description: Inviato a un'applicazione quando il sistema operativo sta per cambiare l'IME corrente. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: Messaggio WM_IME_SELECT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307275"
---
# <a name="wm_ime_select-message"></a>\_Messaggio di \_ selezione IME WM

Inviato a un'applicazione quando il sistema operativo sta per cambiare l'IME corrente. Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*wParam* 
</dt> <dd>

Indicatore di selezione. Questo parametro specifica **true** se l'IME indicato è selezionato. Il parametro è impostato su **false** se l'IME specificato non è più selezionato.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificatore delle impostazioni locali di input associato all'IME.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Un'applicazione che ha creato una finestra IME deve passare questo messaggio alla finestra in modo che sia in grado di recuperare l'handle di layout della tastiera per l'IME appena selezionato.

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  elabora questo messaggio passando le informazioni alla finestra IME predefinita.

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

 

 
