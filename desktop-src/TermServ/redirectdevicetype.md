---
title: Enumerazione RedirectDeviceType
description: Usato per specificare il tipo di un dispositivo.
ms.assetid: B6356217-814E-462F-9DBC-F6D3C0CE129F
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto enumerazione RedirectDeviceType
topic_type:
- apiref
api_name:
- RedirectDeviceType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7058313e7f987589ae17924cce6a95610d997ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301519"
---
# <a name="redirectdevicetype-enumeration"></a>Enumerazione RedirectDeviceType

Usato per specificare il tipo di un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  UsbDevice  = 0
} RedirectDeviceType;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="UsbDevice"></span><span id="usbdevice"></span><span id="USBDEVICE"></span>**UsbDevice**
</dt> <dd>

Un dispositivo USB.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AddDeviceByInstanceId**](imsrdpdevicecollection2-adddevicebyinstanceid.md)
</dt> <dt>

[**RedirectNow**](imsrdpdevicecollection2-redirectnow.md)
</dt> </dl>

 

 





