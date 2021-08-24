---
title: DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS struttura (Wmdrmsdk.h)
description: La struttura DRM MINIMUM OUTPUT PROTECTION LEVELS contiene i livelli minimi di protezione dell'output per la riproduzione \_ di vari tipi di \_ \_ \_ contenuto. Un dispositivo deve supportare l'OPL minimo per un tipo di dati per ricevere tale tipo di dati dal lettore.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS struttura windows Media Format
- Struttura windows Media Format
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5559527507f0399a09661dfe380f51d11e10750eddf7d996b38d110e4f38e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708921"
---
# <a name="drm_minimum_output_protection_levels-structure"></a>Struttura DRM \_ MINIMUM \_ OUTPUT PROTECTION \_ \_ LEVELS

La **struttura DRM \_ MINIMUM OUTPUT \_ PROTECTION \_ \_ LEVELS** contiene i livelli minimi di protezione dell'output per la riproduzione di vari tipi di contenuto. Un dispositivo deve supportare l'OPL minimo per un tipo di dati per ricevere tale tipo di dati dal lettore.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**wCompressedDigitalVideo**
</dt> <dd>

OPL minimo necessario per ricevere video digitale compresso.

</dd> <dt>

**wUncompressedDigitalVideo**
</dt> <dd>

OPL minimo necessario per ricevere video digitali non compressi.

</dd> <dt>

**wAnalogVideo**
</dt> <dd>

OPL minimo necessario per ricevere video analogico.

</dd> <dt>

**wCompressedDigitalAudio**
</dt> <dd>

OPL minimo necessario per ricevere audio digitale compresso.

</dd> <dt>

**wUncompressedDigitalAudio**
</dt> <dd>

OPL minimo necessario per ricevere audio digitale non compresso.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata come membro della struttura [**\_ \_ OPL DRM PLAY.**](drmdrm-play-opl.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





