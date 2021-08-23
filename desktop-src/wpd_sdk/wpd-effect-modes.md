---
description: Il tipo di enumerazione \_ WPD EFFECT MODES descrive vari effetti visivi che possono essere applicati a \_ un'immagine.
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: WPD_EFFECT_MODES enumerazione (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 8ca712a758d23f70d2a1f8760272b821adeec548a1d719c9564cdc8cf17cdeb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657421"
---
# <a name="wpd_effect_modes-enumeration"></a>Enumerazione WPD \_ EFFECT \_ MODES

Il **tipo di enumerazione \_ WPD EFFECT \_ MODES** descrive vari effetti visivi che possono essere applicati a un'immagine.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**MODALITÀ EFFETTO WPD \_ \_ NON \_ DEFINITA**
</dt> <dd>

Non è stato specificato alcun effetto.

</dd> <dt>

<span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**COLORE DELLA MODALITÀ \_ EFFETTO WPD \_ \_**
</dt> <dd>

L'immagine deve essere di colore.

</dd> <dt>

<span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**MODALITÀ EFFETTO WPD \_ \_ IN BIANCO E \_ \_ \_ NERO**
</dt> <dd>

L'immagine deve essere in bianco e nero.

</dd> <dt>

<span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**SEPIA MODALITÀ EFFETTO WPD \_ \_ \_**
</dt> <dd>

L'immagine deve essere sepia.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene usata dalla [proprietà WPD \_ STILL IMAGE EFFECT \_ \_ \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




