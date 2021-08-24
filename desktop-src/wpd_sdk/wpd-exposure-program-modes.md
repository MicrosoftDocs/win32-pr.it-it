---
description: Il tipo di enumerazione WPD EXPOSURE PROGRAM MODES descrive una modalità di esposizione \_ \_ da usare per \_ l'acquisizione di immagini con un dispositivo.
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: WPD_EXPOSURE_PROGRAM_MODES enumerazione (PortableDevice.h)
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
ms.openlocfilehash: dc64012c4f13f84abef55d2426c856b931eb447e61df4f04c69781c089857930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083275"
---
# <a name="wpd_exposure_program_modes-enumeration"></a>Enumerazione WPD \_ EXPOSURE \_ PROGRAM \_ MODES

Il **tipo di enumerazione WPD EXPOSURE PROGRAM \_ \_ \_ MODES** descrive una modalità di esposizione da usare per l'acquisizione di immagini con un dispositivo.

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

<span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**MODALITÀ PROGRAMMA \_ DI ESPOSIZIONE \_ WPD NON \_ \_ DEFINITA**
</dt> <dd>

La modalità di esposizione non è stata specificata.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**MANUALE IN MODALITÀ PROGRAMMA ESPOSIZIONE WPD \_ \_ \_ \_**
</dt> <dd>

L'applicazione deve specificare tutte le impostazioni di esposizione.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**WPD \_ EXPOSURE \_ PROGRAM \_ MODE \_ AUTO**
</dt> <dd>

Usare una modalità di esposizione automatica definita dal dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**PRIORITÀ APERTURA \_ MODALITÀ \_ PROGRAMMA ESPOSIZIONE \_ \_ \_ WPD**
</dt> <dd>

Modalità di esposizione automatica che indica che il valore di apertura dell'obiettivo deve rimanere fisso, ma la velocità dell'otturatore deve essere determinata dal dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**PRIORITÀ DELLA MODALITÀ \_ PROGRAMMA DI \_ ESPOSIZIONE WPD \_ \_ \_**
</dt> <dd>

Modalità di esposizione automatica che indica che la velocità dell'otturatore deve rimanere fissa, ma che l'apertura dell'obiettivo deve essere determinata dal dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD \_ EXPOSURE \_ PROGRAM \_ MODE \_ CREATIVE**
</dt> <dd>

Modalità di esposizione automatica che tenta di ottimizzare la profondità del campo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**AZIONE MODALITÀ PROGRAMMA ESPOSIZIONE WPD \_ \_ \_ \_**
</dt> <dd>

Modalità di esposizione automatica che tenta di ottimizzare la velocità dell'otturatore.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**WPD \_ EXPOSURE \_ PROGRAM \_ MODE \_ PORTRAIT**
</dt> <dd>

Modalità di esposizione automatica che specifica una profondità di campo relativamente superficiale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Indica la modalità del programma di esposizione del dispositivo. Questa enumerazione viene utilizzata dalla [proprietà WPD \_ STILL IMAGE EXPOSURE PROGRAM \_ \_ \_ \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




