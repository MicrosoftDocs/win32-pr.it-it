---
description: Inviato a una finestra quando la funzione SetWindowLong sta per modificare uno o più stili della finestra.
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: WM_STYLECHANGING messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26574f000c23c918bc0dfb14c5ddd0afcbc439939d6719b95da8024b4828f30b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705841"
---
# <a name="wm_stylechanging-message"></a>Messaggio \_ WM STYLECHANGING

Inviato a una finestra quando la [**funzione SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) sta per modificare uno o più stili della finestra.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se gli stili della finestra o gli stili estesi della finestra stanno cambiando. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                            | Significato                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_ EXSTYLE**</dt> <dt>-20</dt> </dl> | Gli stili delle finestre estese sono in modifica.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_ STYLE**</dt> <dt>-16</dt> </dl>       | Gli stili della finestra sono in modifica.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) che contiene i nuovi stili proposti per la finestra. Un'applicazione può esaminare gli stili e, se necessario, modificarli.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**WM \_ STYLECHANGED**](wm-stylechanged.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
