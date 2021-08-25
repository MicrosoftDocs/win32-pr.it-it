---
description: Il tipo di enumerazione WPD POWER SOURCES descrive la fonte di alimentazione utilizzata \_ \_ da un dispositivo.
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: WPD_POWER_SOURCES enumerazione (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_POWER_SOURCES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c31e156caa36e4a60ec74a2e554f983fd35445f28fd1424fbb6395cd2dd63a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026318"
---
# <a name="wpd_power_sources-enumeration"></a>Enumerazione POWER SOURCES WPD \_ \_

Il **tipo di enumerazione \_ WPD POWER \_ SOURCES** descrive la fonte di alimentazione utilizzata da un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**BATTERIA WPD \_ POWER \_ SOURCE \_**
</dt> <dd>

La fonte di alimentazione del dispositivo è una batteria.

</dd> <dt>

<span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**WPD \_ POWER \_ SOURCE \_ EXTERNAL**
</dt> <dd>

Il dispositivo usa una fonte di alimentazione esterna.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla [proprietà \_ WPD DEVICE POWER \_ \_ SOURCE.](device-properties.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




