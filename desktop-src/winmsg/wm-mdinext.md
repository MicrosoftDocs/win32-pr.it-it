---
description: Un'applicazione invia il \_ messaggio WM MDINEXT a una finestra del client di interfaccia a documenti multipli (MDI) per attivare la finestra figlio precedente o successiva.
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: Messaggio WM_MDINEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e0af031c11ea37129e1405e31b07b18f023b7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751207"
---
# <a name="wm_mdinext-message"></a>\_Messaggio MDINEXT WM

Un'applicazione invia il messaggio **WM \_ MDINEXT** a una finestra del client di interfaccia a documenti multipli (MDI) per attivare la finestra figlio precedente o successiva.


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra figlio MDI. Il sistema attiva la finestra figlio immediatamente prima o dopo la finestra figlio specificata, a seconda del valore del parametro *lParam* . Se il parametro *wParam* è **null**, il sistema attiva la finestra figlio immediatamente prima o dopo la finestra figlio attualmente attiva.

</dd> <dt>

*lParam* 
</dt> <dd>

Se questo parametro è zero, il sistema attiva la finestra figlio MDI successiva e posiziona la finestra figlio identificata dal parametro *wParam* dietro tutte le altre finestre figlio. Se questo parametro è diverso da zero, il sistema attiva la finestra figlio precedente, inserendola davanti alla finestra figlio identificata da *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **zero**

Il valore restituito è sempre zero.

## <a name="remarks"></a>Commenti

Se una finestra client MDI riceve un messaggio che modifica l'attivazione delle finestre figlio mentre la finestra figlio MDI attiva è ingrandita, il sistema ripristina la finestra figlio attiva e ingrandisce la finestra figlio appena attivata.

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

[**\_MDIACTIVATE WM**](wm-mdiactivate.md)
</dt> <dt>

[**\_MDIGETACTIVE WM**](wm-mdigetactive.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




