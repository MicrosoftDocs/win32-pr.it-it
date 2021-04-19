---
description: Indica il tipo di dispositivo tablet, ad esempio una penna, un mouse o un digitalizzatore sensibile al tocco.
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: Enumerazione TABLET_DEVICE_KIND
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_DEVICE_KIND
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18f691a2fa909ef28059a4788f4f8b4e184a61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319131"
---
# <a name="tablet_device_kind-enumeration"></a>Enumerazione del tipo di \_ dispositivo Tablet \_

Indica il tipo di dispositivo tablet, ad esempio una penna, un mouse o un digitalizzatore sensibile al tocco.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**\_mouse dispositivo \_ Tablet**
</dt> <dd>

Il tablet è un mouse. Sono inclusi i touchpad presenti in molti computer portatili.

</dd> <dt>

<span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**\_penna del dispositivo Tablet \_**
</dt> <dd>

Il tablet usa una penna elettromagnetica e un digitalizzatore.

</dd> <dt>

<span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**\_tocco del dispositivo Tablet \_**
</dt> <dd>

Il tablet utilizza un digitalizzatore sensibile al tocco.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo ITablet2:: GetDeviceKind**](itablet2-getdevicekind.md)
</dt> </dl>

 

 




