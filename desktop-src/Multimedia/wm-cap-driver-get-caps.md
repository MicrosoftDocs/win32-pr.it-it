---
title: Messaggio di WM_CAP_DRIVER_GET_CAPS (VFW. h)
description: Il \_ messaggio WM Cap \_ driver \_ get \_ Caps restituisce le funzionalità hardware del driver di acquisizione attualmente connesso a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capDriverGetCaps.
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- WM_CAP_DRIVER_GET_CAPS messaggi multimediali di Windows
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
ms.openlocfilehash: 027e530be82c76afebc343ceebe4905daef9b126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518958"
---
# <a name="wm_cap_driver_get_caps-message"></a>\_ \_ \_ Messaggio Caps Get driver di WM Cap \_

Il messaggio **WM \_ Cap \_ driver \_ get \_ Caps** restituisce le funzionalità hardware del driver di acquisizione attualmente connesso a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) .


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

Puntatore alla struttura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) per contenere le funzionalità hardware.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** se la finestra di acquisizione non è connessa a un driver di acquisizione.

## <a name="remarks"></a>Commenti

Le funzionalità restituite in [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) sono costanti per un determinato driver di acquisizione. Le applicazioni devono recuperare queste informazioni una volta quando il driver di acquisizione viene connesso per la prima volta a una finestra di acquisizione.

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

 

 





