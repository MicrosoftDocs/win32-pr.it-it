---
description: Un'applicazione invia il \_ messaggio WM MDIREFRESHMENU a una finestra del client di interfaccia a documenti multipli (MDI) per aggiornare il menu finestra della finestra cornice MDI.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: Messaggio WM_MDIREFRESHMENU (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4eafa7b84dc9389e57d379a30019505e85fb602
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312374"
---
# <a name="wm_mdirefreshmenu-message"></a>\_Messaggio MDIREFRESHMENU WM

Un'applicazione invia il messaggio **WM \_ MDIREFRESHMENU** a una finestra del client di interfaccia a documenti multipli (MDI) per aggiornare il menu finestra della finestra cornice MDI.


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HMENU**

Se il messaggio ha esito positivo, il valore restituito è l'handle per il menu della finestra cornice.

Se il messaggio ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Dopo l'invio di questo messaggio, un'applicazione deve chiamare la funzione [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) per aggiornare la barra dei menu.

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

[**\_MDISETMENU WM**](wm-mdisetmenu.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 
