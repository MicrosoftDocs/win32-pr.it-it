---
description: Il tipo di enumerazione WPD \_ CAPTURE MODES descrive la modalità di temporizzazione di acquisizione di \_ un'acquisizione di immagini ancorate.
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: WPD_CAPTURE_MODES enumerazione (PortableDevice.h)
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
ms.openlocfilehash: c8bc0d667e329db3afccf76497409350d7aa7250b0e6529d0b3f4ddae7a32370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927991"
---
# <a name="wpd_capture_modes-enumeration"></a>Enumerazione WPD \_ CAPTURE \_ MODES

Il **tipo di enumerazione WPD CAPTURE \_ \_ MODES** descrive la modalità di temporizzazione di acquisizione di un'acquisizione di immagini ancorate.

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

<span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**MODALITÀ DI ACQUISIZIONE WPD \_ \_ NON \_ DEFINITA**
</dt> <dd>

La modalità di acquisizione non è stata definita.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**MODALITÀ DI ACQUISIZIONE WPD \_ \_ \_ NORMALE**
</dt> <dd>

Non deve essere usata la modalità di ritardo o burst.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**BURST DELLA MODALITÀ DI ACQUISIZIONE WPD \_ \_ \_**
</dt> <dd>

Specifica che un numero definito di immagini deve essere acquisito con un intervallo definito tra di esse. Il numero di immagini da acquisire e il ritardo temporale tra di esse sono specificati dalle proprietà [WPD \_ STILL IMAGE BURST \_ \_ \_ NUMBER](still-image-properties.md) e [WPD \_ STILL IMAGE BURST \_ \_ \_ INTERVAL.](still-image-properties.md)

</dd> <dt>

<span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**\_ \_ TIMELAPSE DELLA \_ MODALITÀ DI ACQUISIZIONE WPD**
</dt> <dd>

L'acquisizione di immagini deve usare la fotografia time lapse. Il numero di immagini e l'intervallo tra di esse sono descritti dalle proprietà [WPD \_ STILL \_ IMAGE \_ TIMELAPSE \_ NUMBER](still-image-properties.md) e [WPD \_ STILL IMAGE \_ \_ TIMELAPSE \_ INTERVAL.](still-image-properties.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla [proprietà WPD \_ STILL IMAGE CAPTURE \_ \_ \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




