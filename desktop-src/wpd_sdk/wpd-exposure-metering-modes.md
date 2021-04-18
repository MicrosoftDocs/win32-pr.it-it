---
description: Il \_ \_ \_ tipo di enumerazione modalità di misurazione dell'esposizione WPD descrive la modalità di misurazione da usare quando si stima l'esposizione per l'acquisizione di immagini ancora da parte di un dispositivo.
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: Enumerazione WPD_EXPOSURE_METERING_MODES (PortableDevice. h)
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
ms.openlocfilehash: 76c2594339c6fa4997e4d646fc89e8c30dcdf8fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328970"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a>\_Enumerazione delle \_ modalità di misurazione dell'esposizione WPD \_

Il tipo di enumerazione **\_ modalità di \_ misurazione \_ dell'esposizione WPD** descrive la modalità di misurazione da usare quando si stima l'esposizione per l'acquisizione di immagini ancora da parte di un dispositivo.

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

<span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**modalità di misurazione dell'esposizione WPD non \_ \_ \_ \_ definita**
</dt> <dd>

La modalità di misurazione non è definita.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**\_ \_ media modalità di misurazione dell'esposizione \_ WPD \_**
</dt> <dd>

Usare l'esposizione media nell'immagine completa.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**\_ \_ \_ \_ \_ media ponderata del centro modalità di misurazione dell'esposizione \_ WPD**
</dt> <dd>

Utilizzare un'esposizione media, con il centro dell'immagine in base a un peso maggiore.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**\_modalità di misurazione dell'esposizione WPD \_ \_ \_ \_ multispot**
</dt> <dd>

Usare una tecnica di media multispot.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**\_ \_ \_ punto centrale della modalità di misurazione dell' \_ esposizione WPD \_**
</dt> <dd>

Usare una tecnica per la media di punti centrali.

</dd> </dl>

## <a name="remarks"></a>Commenti

Indica la modalità di misurazione del dispositivo. Questa enumerazione viene utilizzata dalla proprietà [della \_ \_ modalità di \_ \_ misurazione \_ dell'esposizione dell'immagine di WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




