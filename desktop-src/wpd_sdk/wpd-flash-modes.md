---
description: Il \_ tipo di enumerazione WPD Flash Modes \_ descrive una modalità flash da usare durante l'acquisizione di immagini con un dispositivo.
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: Enumerazione WPD_FLASH_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 09a2a5b95e86d9d17267cafcfbf723e734ffc74f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328966"
---
# <a name="wpd_flash_modes-enumeration"></a>\_Enumerazione delle \_ modalità flash WPD

Il tipo di enumerazione **WPD \_ Flash \_** Modes descrive una modalità flash da usare durante l'acquisizione di immagini con un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**\_modalità flash WPD non \_ \_ definita**
</dt> <dd>

Non è stata specificata alcuna modalità flash.

</dd> <dt>

<span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**WPD \_ \_ modalità Flash \_ automatica**
</dt> <dd>

Specifica che il flash deve essere usato in modalità automatica, come specificato dal dispositivo.

</dd> <dt>

<span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**\_modalità Flash \_ WPD \_ disabilitata**
</dt> <dd>

Specifica che non deve essere utilizzato alcun flash.

</dd> <dt>

<span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**\_ \_ riempimento modalità Flash \_ WPD**
</dt> <dd>

Specifica un flash di tipo Fill.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD \_ in \_ modalità \_ Flash \_ automatico a occhi rossi \_**
</dt> <dd>

Specifica che deve essere usato il flash di riduzione degli occhi rossi.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**\_riempimento a \_ \_ occhi rossi \_ in modalità flash WPD \_**
</dt> <dd>

Specifica che deve essere usato il flash di riempimento a occhi rossi.

</dd> <dt>

<span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**\_ \_ sincronizzazione esterna in modalità Flash \_ WPD \_**
</dt> <dd>

Specifica che il flash deve essere sincronizzato con altri dispositivi flash esterni.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla proprietà [WPD \_ still \_ Image \_ Flash \_ mode](still-image-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




