---
description: Il \_ \_ tipo di enumerazione modalità di acquisizione WPD descrive la modalità di temporizzazione di acquisizione di un'acquisizione di immagini ancora.
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: Enumerazione WPD_CAPTURE_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326584"
---
# <a name="wpd_capture_modes-enumeration"></a>\_Enumerazione modalità di acquisizione WPD \_

Il tipo di enumerazione **\_ \_ modalità di acquisizione WPD** descrive la modalità di temporizzazione di acquisizione di un'acquisizione di immagini ancora.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**modalità di acquisizione WPD non \_ \_ \_ definita**
</dt> <dd>

La modalità di acquisizione non è stata definita.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**\_modalità di acquisizione WPD \_ \_ normale**
</dt> <dd>

Non è necessario utilizzare la modalità di ritardo o di scatto.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**\_modalità di acquisizione WPD \_ \_**
</dt> <dd>

Specifica che un numero definito di immagini deve essere acquisito con un intervallo definito tra di essi. Il numero di immagini da acquisire e l'intervallo di tempo tra di essi vengono specificate dalle proprietà [WPD \_ still \_ Image \_ \_ numero di picchi](still-image-properties.md) e [WPD \_ still \_ Image \_ \_ ](still-image-properties.md) .

</dd> <dt>

<span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**\_modalità di acquisizione WPD \_ \_ timelapse**
</dt> <dd>

L'acquisizione di immagini deve usare la fotografia time lapse. Il numero di immagini e l'intervallo tra di essi è descritto dalle proprietà [WPD \_ still \_ Image \_ timelapse \_ Number](still-image-properties.md) e [WPD \_ still \_ Image \_ timelapse \_ Interval](still-image-properties.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla proprietà [WPD \_ still \_ Image \_ Capture \_ mode](still-image-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




