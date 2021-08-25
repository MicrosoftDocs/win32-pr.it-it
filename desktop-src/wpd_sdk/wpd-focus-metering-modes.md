---
description: Il tipo di enumerazione WPD FOCUS METERING MODES (MODALITÀ DI MISURAZIONE DELLO STATO ATTIVO WPD) descrive in che modo un dispositivo deve decidere quale parte di un frame usare per \_ \_ impostare lo stato \_ attivo.
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: WPD_FOCUS_METERING_MODES enumerazione (PortableDevice.h)
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
ms.openlocfilehash: eb37cdd32673c385617d9c0c0ae8616c8dae0ab711d1253391ae2c1e6b2f8789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703771"
---
# <a name="wpd_focus_metering_modes-enumeration"></a>Enumerazione WPD \_ FOCUS \_ METERING \_ MODES

Il **tipo di enumerazione WPD FOCUS \_ \_ METERING \_ MODES** (MODALITÀ DI MISURAZIONE DELLO STATO ATTIVO WPD) descrive in che modo un dispositivo deve decidere quale parte di un frame usare per impostare lo stato attivo.

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

<span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**MODALITÀ DI MISURAZIONE DELLO STATO ATTIVO WPD \_ \_ NON \_ \_ DEFINITA**
</dt> <dd>

Indica che non è stata specificata alcuna modalità di messa a fuoco.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**WPD \_ FOCUS \_ METERING \_ MODE \_ CENTER \_ SPOT**
</dt> <dd>

Si concentra sul centro dell'area incorniciata.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**WPD \_ FOCUS \_ METERING \_ MODE \_ MULTI \_ SPOT**
</dt> <dd>

Determinare lo stato attivo analizzando più parti dell'area incorniciata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene specificata dalla proprietà [ \_ WPD STILL IMAGE FOCUS \_ \_ \_ METERING \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




