---
description: Inviato quando una finestra appartenente a un'applicazione diversa da quella attiva sta per essere attivata. Il messaggio viene inviato all'applicazione la cui finestra viene attivata e all'applicazione la cui finestra viene disattivata.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: WM_ACTIVATEAPP messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9afeabe12dfcc36ae7bf2403a7757004847bcf58370f4a0a0904c9bf008e6c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931891"
---
# <a name="wm_activateapp-message"></a>Messaggio \_ WM ACTIVATEAPP

Inviato quando una finestra appartenente a un'applicazione diversa da quella attiva sta per essere attivata. Il messaggio viene inviato all'applicazione la cui finestra viene attivata e all'applicazione la cui finestra viene disattivata.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se la finestra viene attivata o disattivata. Questo parametro è **TRUE se** la finestra viene attivata; è **FALSE se** la finestra viene disattivata.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificatore del thread. Se il *parametro wParam* è **TRUE,** *lParam* è l'identificatore del thread proprietario della finestra disattivata. Se *wParam* è **FALSE,** *lParam* è l'identificatore del thread proprietario della finestra attivata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora questo messaggio, deve restituire zero.

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

[**WM \_ ACTIVATE**](../inputdev/wm-activate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
