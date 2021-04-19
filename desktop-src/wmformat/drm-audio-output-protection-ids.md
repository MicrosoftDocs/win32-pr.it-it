---
title: Struttura DRM_AUDIO_OUTPUT_PROTECTION_IDS (wmdrmsdk. h)
description: La \_ struttura degli \_ ID di protezione dell'output audio DRM \_ \_ contiene un elenco di identificatori di protezione dell'output audio.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- Formato di Windows Media per la struttura DRM_AUDIO_OUTPUT_PROTECTION_IDS
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332283"
---
# <a name="drm_audio_output_protection_ids-structure"></a>\_Struttura degli \_ \_ ID di protezione dell'output audio DRM \_

La struttura degli **\_ ID di \_ \_ protezione \_ dell'output audio DRM** contiene un elenco di identificatori di protezione dell'output audio.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**Centri di**
</dt> <dd>

Numero di voci nella matrice **rgAop** .

</dd> <dt>

**rgAop**
</dt> <dd>

Matrice di strutture di **\_ \_ \_ protezione dell'output audio DRM** . **DRM \_ La \_ \_ protezione dell'output audio** è un tipo definito come [**\_ \_ protezione dell'output DRM**](drm-output-protection.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ \_ ID protezione output audio \_ DRM \_ es.**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**\_ID di \_ protezione dell'output del video DRM \_ \_**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





