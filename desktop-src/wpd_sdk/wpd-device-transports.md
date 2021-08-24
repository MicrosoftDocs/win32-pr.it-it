---
description: Il tipo di enumerazione \_ WPD DEVICE \_ TRANSPORTS specifica la relazione di ereditarietà per un servizio. Questa enumerazione viene usata dalla proprietà \_ WPD DEVICE \_ TRANSPORT.
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: WPD_DEVICE_TRANSPORTS enumerazione (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TRANSPORTS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5f091a84c573038c7d74cf5c2760c298a2542f70f06bdb45d1e72954c9dd5f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703821"
---
# <a name="wpd_device_transports-enumeration"></a>Enumerazione \_ TRANSPORTS DEL DISPOSITIVO WPD \_

Il [**tipo di enumerazione WPD DEVICE \_ \_ TRANSPORTS**](/windows/desktop/wpd_sdk/wpd-device-transports) specifica la relazione di ereditarietà per un servizio. Questa enumerazione viene usata dalla **proprietà \_ WPD DEVICE \_ TRANSPORT.**

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**WPD \_ DEVICE \_ TRANSPORT UNSPECIFIED (TRASPORTO DI DISPOSITIVI WPD \_ NON SPECIFICATO)**
</dt> <dd>

Il tipo di trasporto non è stato specificato.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD \_ DEVICE \_ TRANSPORT \_ USB**
</dt> <dd>

Il dispositivo è connesso tramite USB.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**IP DI TRASPORTO DEL DISPOSITIVO WPD \_ \_ \_**
</dt> <dd>

Il dispositivo è connesso tramite IP (Internet Protocol).

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**BLUETOOTH PER IL \_ TRASPORTO \_ DI DISPOSITIVI \_ WPD**
</dt> <dd>

Il dispositivo è connesso tramite Bluetooth.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

