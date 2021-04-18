---
description: Inviato quando una finestra appartenente a un'applicazione diversa da quella della finestra attiva sta per essere attivata. Il messaggio viene inviato all'applicazione la cui finestra viene attivata e all'applicazione la cui finestra viene disattivata.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: Messaggio WM_ACTIVATEAPP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2d64b90426e004a3c18fdc60538fd21862c42f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314880"
---
# <a name="wm_activateapp-message"></a>\_Messaggio ACTIVATEAPP WM

Inviato quando una finestra appartenente a un'applicazione diversa da quella della finestra attiva sta per essere attivata. Il messaggio viene inviato all'applicazione la cui finestra viene attivata e all'applicazione la cui finestra viene disattivata.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se la finestra viene attivata o disattivata. Questo parametro è **true** se è in corso l'attivazione della finestra; è **false** se la finestra è in fase di disattivazione.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificatore del thread. Se il parametro *wParam* è **true**, *lParam* è l'identificatore del thread a cui appartiene la finestra da disattivare. Se *wParam* è **false**, *lParam* è l'identificatore del thread a cui appartiene la finestra attivata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora il messaggio, deve restituire zero.

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

[**\_attivazione WM**](../inputdev/wm-activate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
