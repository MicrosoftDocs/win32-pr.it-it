---
description: Indica il tipo di dispositivo tablet, ad esempio un digitalizzatore sensibile al tocco, penna o mouse.
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: TABLET_DEVICE_KIND enumerazione
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
ms.openlocfilehash: 784e2393f5470f8abd966ca6dbdce3ac9d9bff734f1245ebd0ef169180c62d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820181"
---
# <a name="tablet_device_kind-enumeration"></a>Enumerazione \_ TABLET DEVICE \_ KIND

Indica il tipo di dispositivo tablet, ad esempio un digitalizzatore sensibile al tocco, penna o mouse.

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

<span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**TABLET \_ DEVICE \_ MOUSE**
</dt> <dd>

Il tablet è un mouse. Sono inclusi i touchpad presenti in molti computer portatili.

</dd> <dt>

<span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**PENNA \_ DEL DISPOSITIVO \_ TABLET**
</dt> <dd>

Il tablet usa una penna e un digitalizzatore di tipo emagnetico.

</dd> <dt>

<span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**TOCCO \_ DEL DISPOSITIVO \_ TABLET**
</dt> <dd>

Il tablet usa un digitalizzatore sensibile al tocco.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo ITablet2::GetDeviceKind**](itablet2-getdevicekind.md)
</dt> </dl>

 

 




