---
description: Un'applicazione invia il messaggio WM MDISETMENU a una finestra client dell'interfaccia a documenti multipli (MDI) per sostituire l'intero menu di una finestra cornice MDI, per sostituire il menu della finestra cornice o \_ entrambi.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: WM_MDISETMENU messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fe87682691c5f113034c20c68cefd81ca3a7018bd44eb868c4f18551cacacd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772071"
---
# <a name="wm_mdisetmenu-message"></a>Messaggio \_ DI WM MDISETMENU

Un'applicazione invia il messaggio **\_ WM MDISETMENU** a una finestra client dell'interfaccia a documenti multipli (MDI) per sostituire l'intero menu di una finestra cornice MDI, per sostituire il menu della finestra cornice o entrambi.


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il nuovo menu della finestra cornice. Se questo parametro è **NULL,** il menu della finestra cornice non viene modificato.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il nuovo menu della finestra. Se questo parametro è **NULL,** il menu della finestra non viene modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HMENU**

Se il messaggio ha esito positivo, il valore restituito è l'handle del menu della finestra cornice precedente.

Se il messaggio ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Dopo aver inviato questo messaggio, un'applicazione deve chiamare la [**funzione DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) per aggiornare la barra dei menu.

Se questo messaggio sostituisce il menu della finestra, le voci di menu della finestra figlio MDI vengono rimosse dal menu della finestra precedente e aggiunte al nuovo menu della finestra.

Se una finestra figlio MDI è ingrandita e questo messaggio sostituisce il menu della finestra cornice MDI, l'icona del menu della finestra e l'icona di ripristino vengono rimosse dal menu della finestra cornice precedente e aggiunte al nuovo menu della finestra cornice.

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

[**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[**WM \_ MDIREFRESHMENU**](wm-mdirefreshmenu.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 
