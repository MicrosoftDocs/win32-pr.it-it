---
description: Specifica la relazione di ereditarietà per un servizio.
ms.assetid: e7f5314a-75e8-4f36-8e18-d614eda7a097
title: WPD_SERVICE_INHERITANCE_TYPES enumerazione (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SERVICE_INHERITANCE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5a0e69986e7415a5a12eca7c450b0d7ff064c650d33c35997b9a166b01592c41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444801"
---
# <a name="wpd_service_inheritance_types-enumeration"></a>Enumerazione WPD \_ SERVICE \_ INHERITANCE \_ TYPES

Il **tipo di enumerazione WPD SERVICE INHERITANCE \_ \_ \_ TYPES** specifica la relazione di ereditarietà per un servizio.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWPD_SERVICE_INHERITANCE_TYPES { 
  WPD_SERVICE_INHERITANCE_IMPLEMENTATION  = 0
} WPD_SERVICE_INHERITANCE_TYPES;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**IMPLEMENTAZIONE \_ DELL'EREDITARIETÀ \_ DEL SERVIZIO WPD \_**
</dt> <dd>

Il servizio eredita implementando una definizione di servizio astratta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPortableDeviceServiceCapabilities::GetInheritedServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getinheritedservices)
</dt> </dl>

 

 




