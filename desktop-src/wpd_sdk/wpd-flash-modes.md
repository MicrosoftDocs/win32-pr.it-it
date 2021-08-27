---
description: Il tipo di enumerazione \_ WPD FLASH MODES descrive una modalità flash da usare per \_ l'acquisizione di immagini con un dispositivo.
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: WPD_FLASH_MODES enumerazione (PortableDevice.h)
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
ms.openlocfilehash: 72e9b6cb2b52f1d90c584b6f425711769b25ea0c5d44065b5aa377d2811592e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005921"
---
# <a name="wpd_flash_modes-enumeration"></a>Enumerazione WPD \_ FLASH \_ MODES

Il **tipo di enumerazione \_ WPD FLASH \_ MODES** descrive una modalità flash da usare per l'acquisizione di immagini con un dispositivo.

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

<span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**MODALITÀ FLASH WPD \_ \_ NON \_ DEFINITA**
</dt> <dd>

Non è stata specificata alcuna modalità flash.

</dd> <dt>

<span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**MODALITÀ FLASH WPD \_ \_ \_ AUTOMATICA**
</dt> <dd>

Specifica che la memoria flash deve essere usata in modalità automatica, come specificato dal dispositivo.

</dd> <dt>

<span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**MODALITÀ FLASH WPD \_ \_ \_ DISATTIVATA**
</dt> <dd>

Specifica che non deve essere usata alcuna memoria flash.

</dd> <dt>

<span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**RIEMPIMENTO IN MODALITÀ FLASH WPD \_ \_ \_**
</dt> <dd>

Specifica un flash di tipo riempimento.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD \_ FLASH \_ MODE \_ RED \_ EYE \_ AUTO**
</dt> <dd>

Specifica che deve essere usato il flash di riduzione oculare rosso.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**WPD FLASH MODE RED EYE FILL (RIEMPIMENTO \_ \_ \_ OCULARE ROSSO IN MODALITÀ FLASH \_ \_ WPD)**
</dt> <dd>

Specifica che deve essere usato il flash di riempimento a occhio rosso.

</dd> <dt>

<span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**SINCRONIZZAZIONE ESTERNA IN MODALITÀ FLASH WPD \_ \_ \_ \_**
</dt> <dd>

Specifica che la memoria flash deve essere sincronizzata con altri dispositivi flash esterni.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene usata dalla [proprietà \_ WPD STILL IMAGE FLASH \_ \_ \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




