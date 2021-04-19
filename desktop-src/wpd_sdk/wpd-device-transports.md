---
description: Il \_ \_ tipo di enumerazione trasporti dispositivi WPD specifica la relazione di ereditarietà per un servizio. Questa enumerazione viene utilizzata dalla proprietà di \_ trasporto del dispositivo WPD \_ .
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: Enumerazione WPD_DEVICE_TRANSPORTS (PortableDevice. h)
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
ms.openlocfilehash: 574c6b0b00980d110f2374e7426dd101c9122854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324208"
---
# <a name="wpd_device_transports-enumeration"></a>\_ \_ Enumerazione trasporti dispositivi WPD

Il tipo di enumerazione [**\_ \_ trasporti dispositivi WPD**](/windows/desktop/wpd_sdk/wpd-device-transports) specifica la relazione di ereditarietà per un servizio. Questa enumerazione viene utilizzata dalla proprietà **di \_ \_ trasporto del dispositivo WPD** .

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

<span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**WPD \_ trasporto dispositivo non \_ \_ specificato**
</dt> <dd>

Tipo di trasporto non specificato.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**\_ \_ USB trasporto dispositivi \_ WPD**
</dt> <dd>

Il dispositivo è connesso tramite USB.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**\_ \_ IP trasporto dispositivi \_ WPD**
</dt> <dd>

Il dispositivo è connesso tramite Internet Protocol (IP).

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**\_ \_ Bluetooth trasporto dispositivi \_ WPD**
</dt> <dd>

Il dispositivo è connesso tramite Bluetooth.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

