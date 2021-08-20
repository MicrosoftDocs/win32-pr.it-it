---
title: WM_CAP_DRIVER_GET_CAPS messaggio (Vfw.h)
description: Il messaggio WM \_ CAP DRIVER GET CAPS restituisce le funzionalità hardware del driver di acquisizione attualmente connesso a una finestra di \_ \_ \_ acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro capDriverGetCaps.
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- WM_CAP_DRIVER_GET_CAPS messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_CAPS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aecc863234cddf64bece47896015fd01e97093d227951aef69363136e55cabe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687081"
---
# <a name="wm_cap_driver_get_caps-message"></a>Messaggio \_ GET \_ \_ \_ CAPS del DRIVER WM CAP

Il **messaggio WM CAP DRIVER GET \_ \_ \_ \_ CAPS** restituisce le funzionalità hardware del driver di acquisizione attualmente connesso a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capDriverGetCaps.**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps)


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Dimensione, in byte, della struttura a cui fa riferimento **s**.

</dd> <dt>

<span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*
</dt> <dd>

Puntatore alla [**struttura CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) per contenere le funzionalità hardware.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o **FALSE** se la finestra di acquisizione non è connessa a un driver di acquisizione.

## <a name="remarks"></a>Commenti

Le funzionalità restituite in [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) sono costanti per un determinato driver di acquisizione. Le applicazioni devono recuperare queste informazioni una sola volta quando il driver di acquisizione è connesso per la prima volta a una finestra di acquisizione.

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

 

 





