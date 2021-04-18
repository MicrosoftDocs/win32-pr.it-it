---
title: Messaggio di WM_CAP_DRIVER_GET_VERSION (VFW. h)
description: Il \_ messaggio WM Cap \_ driver \_ get \_ Version restituisce le informazioni sulla versione del driver di acquisizione connesso a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capDriverGetVersion.
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- WM_CAP_DRIVER_GET_VERSION messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced70f2d0159ef4bbad3f2d7a8027c30b2c71a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302346"
---
# <a name="wm_cap_driver_get_version-message"></a>\_Messaggio di \_ versione del driver WM Cap \_ get \_

Il messaggio **WM \_ Cap \_ driver \_ get \_ Version** restituisce le informazioni sulla versione del driver di acquisizione connesso a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) .


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Dimensione, in byte, del buffer definito dall'applicazione a cui fa riferimento **szVer**.

</dd> <dt>

<span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*
</dt> <dd>

Puntatore a un buffer definito dall'applicazione utilizzato per restituire le informazioni sulla versione come stringa con terminazione null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** se la finestra di acquisizione non è connessa a un driver di acquisizione.

## <a name="remarks"></a>Commenti

Le informazioni sulla versione sono una stringa di testo recuperata dall'area delle risorse del driver. Le applicazioni devono allocare circa 40 byte per questa stringa. Se le informazioni sulla versione non sono disponibili, viene restituita una stringa **null** .

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

 

 





