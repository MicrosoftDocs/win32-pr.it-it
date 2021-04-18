---
description: Inviato a una finestra che l'utente sta muovendo. Elaborando questo messaggio, un'applicazione può monitorare la posizione del rettangolo di trascinamento e, se necessario, modificarne la posizione.
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: Messaggio WM_MOVING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5847189d64601ec999321920ead716fbdf22e2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306658"
---
# <a name="wm_moving-message"></a>\_Messaggio di trasferimento WM

Inviato a una finestra che l'utente sta muovendo. Elaborando questo messaggio, un'applicazione può monitorare la posizione del rettangolo di trascinamento e, se necessario, modificarne la posizione.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOVING                       0x0216
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) con la posizione corrente della finestra, in coordinate dello schermo. Per modificare la posizione del rettangolo di trascinamento, un'applicazione deve modificare i membri di questa struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Un'applicazione deve restituire **true** se elabora questo messaggio.

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

[**\_spostamento WM**](wm-move.md)
</dt> <dt>

[**\_dimensionamento WM**](wm-sizing.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
