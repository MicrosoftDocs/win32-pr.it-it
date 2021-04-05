---
description: Un'applicazione invia il \_ messaggio WM MDIDESTROY a una finestra del client di interfaccia a documenti multipli (MDI) per chiudere una finestra figlio MDI.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: Messaggio WM_MDIDESTROY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edea8fe8dadc691ca912df4e9ee5d57421124bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751210"
---
# <a name="wm_mdidestroy-message"></a>\_Messaggio MDIDESTROY WM

Un'applicazione invia il messaggio **WM \_ MDIDESTROY** a una finestra del client di interfaccia a documenti multipli (MDI) per chiudere una finestra figlio MDI.


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra figlio MDI da chiudere.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **zero**

Questo messaggio restituisce sempre zero.

## <a name="remarks"></a>Commenti

Questo messaggio rimuove il titolo della finestra figlio MDI dalla finestra cornice MDI e disattiva la finestra figlio. Per chiudere tutte le finestre figlio MDI, un'applicazione deve utilizzare questo messaggio.

Se una finestra client MDI riceve un messaggio che modifica l'attivazione delle finestre figlio e la finestra figlio MDI attiva è ingrandita, il sistema ripristina la finestra figlio attiva e ingrandisce la finestra figlio appena attivata.

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

[**\_MDICREATE WM**](wm-mdicreate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




