---
title: WM_CAP_GET_MCI_DEVICE messaggio (Vfw.h)
description: Il messaggio WM CAP GET MCI DEVICE recupera il nome di un dispositivo MCI impostato in precedenza con il messaggio \_ \_ WM CAP SET \_ \_ \_ \_ \_ MCI \_ DEVICE. È possibile inviare questo messaggio in modo esplicito o usando la macro capGetMCIDeviceName.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- WM_CAP_GET_MCI_DEVICE di Windows multimediali
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
ms.openlocfilehash: b9471177693bfbd5646d93e8487395cdf330b8281a1f43fa00d79dc690e6d718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800655"
---
# <a name="wm_cap_get_mci_device-message"></a>Messaggio \_ WM CAP GET \_ \_ MCI \_ DEVICE

Il **messaggio WM CAP GET \_ \_ \_ MCI \_ DEVICE** recupera il nome di un dispositivo MCI impostato in precedenza con il messaggio [**WM CAP SET \_ \_ \_ MCI \_ DEVICE.**](wm-cap-set-mci-device.md) È possibile inviare questo messaggio in modo esplicito o usando la macro [**capGetMCIDeviceName.**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename)


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Lunghezza, in byte, del buffer a cui fa **riferimento szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Puntatore a una stringa con terminazione Null che contiene il nome del dispositivo MCI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

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

 

 





