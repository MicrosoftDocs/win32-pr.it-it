---
title: Messaggio di WM_CAP_GET_MCI_DEVICE (VFW. h)
description: Il \_ messaggio WM Cap \_ get \_ MCI \_ Device Recupera il nome di un dispositivo MCI precedentemente impostato con il \_ messaggio di dispositivo WM Cap \_ set \_ MCI \_ . È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capGetMCIDeviceName.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- WM_CAP_GET_MCI_DEVICE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0960ff9aa1366802611f444383212c4bcc45bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475071"
---
# <a name="wm_cap_get_mci_device-message"></a>\_Messaggio del dispositivo WM Cap \_ get \_ MCI \_

Il messaggio **WM \_ Cap \_ get \_ MCI \_ Device** Recupera il nome di un dispositivo MCI precedentemente impostato con il messaggio di [**\_ dispositivo WM Cap \_ set \_ MCI \_**](wm-cap-set-mci-device.md) . È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) .


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Lunghezza, in byte, del buffer a cui fa riferimento **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome del dispositivo MCI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

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

 

 





