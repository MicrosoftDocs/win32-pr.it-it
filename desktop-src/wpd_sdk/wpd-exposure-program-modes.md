---
description: Il \_ \_ tipo di enumerazione WPD Exposure Program Modes \_ descrive una modalità di esposizione da usare per l'acquisizione di immagini con un dispositivo.
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: Enumerazione WPD_EXPOSURE_PROGRAM_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_PROGRAM_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a88ce90bb9e776cd45245b32a363635c2ccf0560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328968"
---
# <a name="wpd_exposure_program_modes-enumeration"></a>\_Enumerazione WPD Exposure \_ Program \_ modes

Il tipo di enumerazione **WPD \_ Exposure \_ Program \_** Modes descrive una modalità di esposizione da usare per l'acquisizione di immagini con un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_EXPOSURE_PROGRAM_MODES { 
  WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED          = 0,
  WPD_EXPOSURE_PROGRAM_MODE_MANUAL             = 1,
  WPD_EXPOSURE_PROGRAM_MODE_AUTO               = 2,
  WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY  = 3,
  WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY   = 4,
  WPD_EXPOSURE_PROGRAM_MODE_CREATIVE           = 5,
  WPD_EXPOSURE_PROGRAM_MODE_ACTION             = 6,
  WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT           = 7
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**\_modalità programma esposizione WPD non \_ \_ \_ definita**
</dt> <dd>

La modalità di esposizione non è stata specificata.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**\_ \_ \_ manuale modalità programma esposizione \_ WPD**
</dt> <dd>

L'applicazione deve specificare tutte le impostazioni di esposizione.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**\_ \_ modalità programma esposizione \_ WPD \_ auto**
</dt> <dd>

Usare una modalità di esposizione automatica definita dal dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**\_priorità di \_ \_ apertura della modalità programma WPD Exposure \_ \_**
</dt> <dd>

Modalità di esposizione automatica che indica che il valore di apertura della lente deve rimanere fisso, ma la velocità dell'otturatore deve essere determinata dal dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**\_priorità di \_ \_ Shutter della modalità programma WPD Exposure \_ \_**
</dt> <dd>

Modalità di esposizione automatica che indica che la velocità dell'otturatore deve rimanere fissa, ma tale apertura della lente dovrebbe essere determinata dal dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**\_creazione della \_ \_ modalità programma esposizione WPD \_**
</dt> <dd>

Modalità di esposizione automatica che tenta di ottimizzare la profondità del campo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**\_ \_ \_ azione modalità programma esposizione \_ WPD**
</dt> <dd>

Modalità di esposizione automatica che tenta di massimizzare la velocità dell'otturatore.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**\_ \_ \_ verticale modalità programma esposizione \_ WPD**
</dt> <dd>

Modalità di esposizione automatica che specifica una profondità relativamente superficiale del campo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Indica la modalità del programma di esposizione del dispositivo. Questa enumerazione viene utilizzata dalla proprietà [ \_ \_ \_ \_ \_ modalità programma WPD Still Image Exposure](still-image-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




