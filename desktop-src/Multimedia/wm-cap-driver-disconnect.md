---
title: WM_CAP_DRIVER_DISCONNECT messaggio (Vfw.h)
description: Il messaggio WM \_ CAP DRIVER DISCONNECT disconnette un driver di acquisizione da una finestra di \_ \_ acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro capDriverDisconnect.
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- WM_CAP_DRIVER_DISCONNECT messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6365366c6ea37b36734262d1d7a8412a7729406ff3fcc12e10ae9ba55d9ba84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803861"
---
# <a name="wm_cap_driver_disconnect-message"></a>Messaggio \_ DI \_ DISCONNESSIONE DEL DRIVER CAP WM \_

Il **messaggio WM CAP DRIVER \_ \_ \_ DISCONNECT** disconnette un driver di acquisizione da una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capDriverDisconnect.**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect)


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o **FALSE** se la finestra di acquisizione non è connessa a un driver di acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





