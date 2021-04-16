---
description: Inviato a una finestra dopo che la funzione SetWindowLong ha modificato uno o più stili della finestra.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: Messaggio WM_STYLECHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5429db06dea95dbbc003e432a2b619c5cf8d056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529833"
---
# <a name="wm_stylechanged-message"></a>\_Messaggio STYLECHANGED WM

Inviato a una finestra dopo che la funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) ha modificato uno o più stili della finestra.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se gli stili o gli stili della finestra estesa della finestra sono stati modificati. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                            | Significato                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_ EXSTYLE**</dt> <dt>-20</dt> </dl> | Gli stili estesi della finestra sono stati modificati.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_ STILE**</dt> <dt>-16</dt> </dl>       | Gli stili della finestra sono stati modificati.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) che contiene i nuovi stili per la finestra. Un'applicazione può esaminare gli stili, ma non modificarli.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Un'applicazione deve restituire zero se elabora questo messaggio.

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

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**\_STYLECHANGING WM**](wm-stylechanging.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
