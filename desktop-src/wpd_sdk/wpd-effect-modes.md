---
description: Il \_ \_ tipo di enumerazione WPD Effect Modes descrive vari effetti visivi che possono essere applicati a un'immagine.
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: Enumerazione WPD_EFFECT_MODES (PortableDevice. h)
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
ms.openlocfilehash: 7e29f89207a74d335fbe1c2561f8dcf9cec3e923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324205"
---
# <a name="wpd_effect_modes-enumeration"></a>\_Enumerazione WPD Effect \_ modes

Il tipo di enumerazione **WPD \_ Effect \_ modes** descrive vari effetti visivi che possono essere applicati a un'immagine.

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

<span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**\_modalità effetto WPD non \_ \_ definita**
</dt> <dd>

Nessun effetto specificato.

</dd> <dt>

<span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**\_ \_ colore modalità effetto \_ WPD**
</dt> <dd>

L'immagine deve essere color.

</dd> <dt>

<span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**\_modalità effetto WPD in \_ \_ \_ \_ bianco e nero**
</dt> <dd>

L'immagine deve essere nera e bianca.

</dd> <dt>

<span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**\_ \_ seppia modalità effetto \_ WPD**
</dt> <dd>

L'immagine deve essere di seppia.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla proprietà [WPD \_ still \_ Image \_ Effect \_ mode](still-image-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




