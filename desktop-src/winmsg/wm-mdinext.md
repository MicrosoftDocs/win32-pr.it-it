---
description: Un'applicazione invia il messaggio WM MDINEXT a una finestra \_ client MDI (Multiple Document Interface) per attivare la finestra figlio successiva o precedente.
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: WM_MDINEXT messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa2b88e5368db2a6b700e0b4d469d1ba680d3caa4d2c1e1c208c5143660396f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931241"
---
# <a name="wm_mdinext-message"></a>Messaggio \_ WM MDINEXT

Un'applicazione invia il **messaggio \_ WM MDINEXT** a una finestra client MDI (Multiple Document Interface) per attivare la finestra figlio successiva o precedente.


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra figlio MDI. Il sistema attiva la finestra figlio immediatamente prima o dopo la finestra figlio specificata, a seconda del valore del *parametro lParam.* Se il *parametro wParam* è **NULL,** il sistema attiva la finestra figlio immediatamente prima o dopo la finestra figlio attualmente attiva.

</dd> <dt>

*lParam* 
</dt> <dd>

Se questo parametro è zero, il sistema attiva la finestra figlio MDI successiva e posiziona la finestra figlio identificata dal *parametro wParam* dietro tutte le altre finestre figlio. Se questo parametro è diverso da zero, il sistema attiva la finestra figlio precedente, posizionandola davanti alla finestra figlio identificata da *wParam*.

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
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**WM \_ MDIACTIVATE**](wm-mdiactivate.md)
</dt> <dt>

[**WM \_ MDIGETACTIVE**](wm-mdigetactive.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




