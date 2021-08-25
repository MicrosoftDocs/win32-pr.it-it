---
title: WM_CAP_GET_USER_DATA messaggio (Vfw.h)
description: Il messaggio WM \_ CAP GET USER DATA recupera un valore di dati LONG \_ \_ \_ \_ PTR associato a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro capGetUserData.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- WM_CAP_GET_USER_DATA di Windows multimediali
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a79a513d415d166ab2715a181a6d8fc366b60480caf2982f6bbc53eadf90d96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892031"
---
# <a name="wm_cap_get_user_data-message"></a>Messaggio WM \_ CAP \_ GET USER \_ \_ DATA

Il **messaggio WM CAP GET USER \_ \_ \_ \_ DATA** recupera un **valore di dati LONG \_ PTR** associato a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capGetUserData.**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata)


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce un valore salvato in precedenza usando il [**messaggio WM CAP SET \_ \_ \_ USER \_**](wm-cap-set-user-data.md) DATA.

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

 

 





