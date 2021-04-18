---
description: Un'applicazione invia il \_ messaggio WM MDISETMENU a una finestra del client di interfaccia a documenti multipli (MDI) per sostituire l'intero menu di una finestra cornice MDI, per sostituire il menu finestra della finestra cornice o entrambi.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: Messaggio WM_MDISETMENU (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74b90aed079482e2d2b666432f72c15d6ca27896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312373"
---
# <a name="wm_mdisetmenu-message"></a>\_Messaggio MDISETMENU WM

Un'applicazione invia il messaggio **WM \_ MDISETMENU** a una finestra del client di interfaccia a documenti multipli (MDI) per sostituire l'intero menu di una finestra cornice MDI, per sostituire il menu finestra della finestra cornice o entrambi.


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il nuovo menu della finestra cornice. Se questo parametro è **null**, il menu della finestra cornice non viene modificato.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il menu nuova finestra. Se questo parametro è **null**, il menu finestra non viene modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HMENU**

Se il messaggio ha esito positivo, il valore restituito è l'handle per il vecchio menu della finestra cornice.

Se il messaggio ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Dopo l'invio di questo messaggio, un'applicazione deve chiamare la funzione [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) per aggiornare la barra dei menu.

Se questo messaggio sostituisce il menu finestra, le voci di menu finestra figlio MDI vengono rimosse dal menu finestra precedente e aggiunte al menu nuova finestra.

Se una finestra figlio MDI viene ingrandita e questo messaggio sostituisce il menu della finestra cornice MDI, l'icona del menu finestra e l'icona di ripristino vengono rimossi dal menu della finestra cornice precedente e aggiunti al menu nuova finestra cornice.

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

[**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[**\_MDIREFRESHMENU WM**](wm-mdirefreshmenu.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 
