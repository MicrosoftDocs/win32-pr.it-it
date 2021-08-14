---
description: Un'applicazione invia il messaggio WM MDIREFRESHMENU a una finestra client MDI (Multiple Document Interface) per aggiornare il menu della finestra della \_ finestra cornice MDI.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: WM_MDIREFRESHMENU messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 707059d3cc51703819968f929f9692dbb2422ee3f9fa77e2edb697f12257faf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200067"
---
# <a name="wm_mdirefreshmenu-message"></a>Messaggio di WM \_ MDIREFRESHMENU

Un'applicazione invia il messaggio **\_ WM MDIREFRESHMENU** a una finestra client dell'interfaccia a documenti multipli (MDI) per aggiornare il menu della finestra della finestra cornice MDI.


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HMENU**

Se il messaggio ha esito positivo, il valore restituito è l'handle per il menu della finestra cornice.

Se il messaggio ha esito negativo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

Dopo aver inviato questo messaggio, un'applicazione deve chiamare la [**funzione DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) per aggiornare la barra dei menu.

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

[**WM \_ MDISETMENU**](wm-mdisetmenu.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 
