---
title: Messaggio di WM_CAP_GET_USER_DATA (VFW. h)
description: Il \_ messaggio WM Cap \_ get \_ User \_ Data recupera un \_ valore di dati ptr lungo associato a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capGetUserData.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- WM_CAP_GET_USER_DATA messaggi multimediali di Windows
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
ms.openlocfilehash: 02951667600acba115f506a610b167b72b69ea99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518634"
---
# <a name="wm_cap_get_user_data-message"></a>\_ \_ \_ Messaggio dati utente per ottenere WM Cap \_

Il messaggio **WM \_ Cap \_ get \_ User \_ Data** recupera un valore di dati **\_ ptr lungo** associato a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) .


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce un valore salvato in precedenza utilizzando il messaggio di [**\_ \_ \_ \_ dati utente per l'impostazione di WM Cap**](wm-cap-set-user-data.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





