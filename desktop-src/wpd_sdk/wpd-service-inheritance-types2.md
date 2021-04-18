---
description: Specifica la relazione di ereditarietà per un servizio.
ms.assetid: e7f5314a-75e8-4f36-8e18-d614eda7a097
title: Enumerazione WPD_SERVICE_INHERITANCE_TYPES (PortableDevice. h)
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
ms.openlocfilehash: ad9115bf7bb0912362455986e77d5792cceec3b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325103"
---
# <a name="wpd_service_inheritance_types-enumeration"></a>\_ \_ Enumerazione tipi ereditarietà servizio WPD \_

Il tipo di enumerazione dei **\_ tipi di \_ ereditarietà \_ del servizio WPD** specifica la relazione di ereditarietà per un servizio.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWPD_SERVICE_INHERITANCE_TYPES { 
  WPD_SERVICE_INHERITANCE_IMPLEMENTATION  = 0
} WPD_SERVICE_INHERITANCE_TYPES;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**\_implementazione dell' \_ ereditarietà del servizio WPD \_**
</dt> <dd>

Il servizio eredita implementando una definizione del servizio abstract.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPortableDeviceServiceCapabilities::GetInheritedServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getinheritedservices)
</dt> </dl>

 

 




