---
description: Il tipo di enumerazione WPD EXPOSURE METERING MODES descrive la modalità di misurazione da usare per stimare l'esposizione per l'acquisizione di immagini statiche \_ da parte di un \_ \_ dispositivo.
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: WPD_EXPOSURE_METERING_MODES enumerazione (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2a165493142fc25ea64adc2678e8bc4ccbeace32e245422f0fcea419063a26ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842281"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a>Enumerazione WPD \_ EXPOSURE \_ METERING \_ MODES

Il **tipo di enumerazione WPD EXPOSURE \_ \_ METERING \_ MODES** descrive la modalità di misurazione da usare per stimare l'esposizione per l'acquisizione di immagini statiche da parte di un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**MODALITÀ DI \_ MISURAZIONE \_ DELL'ESPOSIZIONE WPD \_ \_ NON DEFINITA**
</dt> <dd>

La modalità di misurazione non è definita.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**MEDIA MODALITÀ DI \_ \_ MISURAZIONE \_ DELL'ESPOSIZIONE \_ WPD**
</dt> <dd>

Usare l'esposizione media nell'intera immagine.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**MEDIA PONDERATA PONDERATA DELLA MODALITÀ DI \_ \_ \_ MISURAZIONE DELL'ESPOSIZIONE \_ \_ \_ WPD**
</dt> <dd>

Usare un'esposizione media, con il centro dell'immagine con un peso maggiore.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**MODALITÀ DI \_ MISURAZIONE \_ DELL'ESPOSIZIONE WPD \_ \_ MULTI \_ SPOT**
</dt> <dd>

Usare una tecnica di media multi-spot.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**PUNTO CENTRALE DELLA \_ MODALITÀ \_ DI MISURAZIONE DELL'ESPOSIZIONE \_ \_ WPD \_**
</dt> <dd>

Usare una tecnica di media del punto centrale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Indica la modalità di misurazione del dispositivo. Questa enumerazione viene utilizzata dalla [proprietà WPD \_ STILL IMAGE EXPOSURE \_ \_ \_ METERING \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




