---
description: Il tipo di enumerazione WPD Power Sources \_ \_ descrive la fonte di alimentazione usata da un dispositivo.
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: Enumerazione WPD_POWER_SOURCES (PortableDevice. h)
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
ms.openlocfilehash: bf9a153d4d41a64b639f796ea2ba0eeb9e567a32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325801"
---
# <a name="wpd_power_sources-enumeration"></a>\_ \_ Enumerazione origini alimentazione WPD

Il tipo di enumerazione **WPD \_ Power \_** Sources descrive la fonte di alimentazione usata da un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**\_batteria di \_ origine \_ alimentazione WPD**
</dt> <dd>

La fonte di alimentazione del dispositivo è una batteria.

</dd> <dt>

<span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**\_origine alimentazione \_ \_ esterna WPD**
</dt> <dd>

Il dispositivo usa una fonte di alimentazione esterna.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla proprietà [di \_ \_ \_ origine dell'alimentazione del dispositivo WPD](device-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




