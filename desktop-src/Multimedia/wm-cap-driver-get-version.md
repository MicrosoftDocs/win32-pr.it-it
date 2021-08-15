---
title: WM_CAP_DRIVER_GET_VERSION messaggio (Vfw.h)
description: Il messaggio WM \_ CAP DRIVER GET VERSION restituisce le informazioni sulla versione del driver di acquisizione connesso a una \_ finestra di \_ \_ acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro capDriverGetVersion.
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- WM_CAP_DRIVER_GET_VERSION di messaggi Windows multimediali
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
ms.openlocfilehash: 49f6bed4513383c5dd889639a78e9f00e409fe347bfd6b64b112ea830571ae55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687091"
---
# <a name="wm_cap_driver_get_version-message"></a>Messaggio GET VERSION del DRIVER WM \_ CAP \_ \_ \_

Il **messaggio WM CAP DRIVER GET \_ \_ \_ \_ VERSION** restituisce le informazioni sulla versione del driver di acquisizione connesso a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capDriverGetVersion.**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion)


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Dimensione, in byte, del buffer definito dall'applicazione a cui fa riferimento **szVer.**

</dd> <dt>

<span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*
</dt> <dd>

Puntatore a un buffer definito dall'applicazione utilizzato per restituire le informazioni sulla versione come stringa con terminazione Null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** ha esito positivo o **FALSE** se la finestra di acquisizione non è connessa a un driver di acquisizione.

## <a name="remarks"></a>Commenti

Le informazioni sulla versione sono una stringa di testo recuperata dall'area delle risorse del driver. Le applicazioni devono allocare circa 40 byte per questa stringa. Se le informazioni sulla versione non sono disponibili, viene **restituita** una stringa NULL.

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

 

 





