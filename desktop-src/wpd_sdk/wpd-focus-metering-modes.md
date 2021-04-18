---
description: Il \_ tipo di enumerazione modalità di misurazione dello stato attivo WPD \_ descrive il \_ modo in cui un dispositivo deve decidere quale parte di un frame utilizzare per impostare lo stato attivo.
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: Enumerazione WPD_FOCUS_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f59d6a2f1cabbbe7b072a87caa3e5d74d012fc49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328965"
---
# <a name="wpd_focus_metering_modes-enumeration"></a>\_Enumerazione delle \_ modalità di misurazione dello stato attivo WPD \_

Il tipo di enumerazione **\_ modalità di \_ misurazione \_ dello stato attivo WPD** descrive il modo in cui un dispositivo deve decidere quale parte di un frame utilizzare per impostare lo stato attivo.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**\_modalità di misurazione dello stato attivo WPD non \_ \_ \_ definita**
</dt> <dd>

Indica che non è stata specificata alcuna modalità di messa a fuoco.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**\_ \_ \_ punto centrale della modalità di misurazione dello \_ stato attivo \_ WPD**
</dt> <dd>

Si concentra sul centro dell'area incorniciata.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**\_modalità di misurazione dello stato attivo WPD \_ \_ \_ \_ multispot**
</dt> <dd>

Determinare lo stato attivo analizzando più parti dell'area incorniciata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene specificata dalla proprietà della [modalità di misurazione dello stato di WPD \_ still \_ Image \_ \_ \_ ](still-image-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




