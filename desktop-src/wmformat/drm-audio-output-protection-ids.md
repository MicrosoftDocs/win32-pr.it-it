---
title: DRM_AUDIO_OUTPUT_PROTECTION_IDS struttura (Wmdrmsdk.h)
description: La struttura DRM \_ AUDIO \_ OUTPUT PROTECTION \_ \_ IDS contiene un elenco di identificatori di protezione dell'output audio.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS struttura windows Media Format
- Struttura windows Media Format
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
ms.openlocfilehash: 7e31589a229dcd5e32a0198cf7f3679846574bdb605e25a8df272b1793704b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659011"
---
# <a name="drm_audio_output_protection_ids-structure"></a>Struttura DRM \_ AUDIO \_ OUTPUT PROTECTION \_ \_ IDS

La **struttura DRM \_ AUDIO OUTPUT \_ PROTECTION \_ \_ IDS** contiene un elenco di identificatori di protezione dell'output audio.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**cEntries**
</dt> <dd>

Numero di voci nella matrice **rgAop.**

</dd> <dt>

**rgAop**
</dt> <dd>

Matrice di **strutture DRM \_ AUDIO OUTPUT \_ \_ PROTECTION.** **DRM \_ AUDIO \_ OUTPUT \_ PROTECTION** è un tipo definito come [**DRM OUTPUT \_ \_ PROTECTION.**](drm-output-protection.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID PROTEZIONE OUTPUT AUDIO DRM \_ \_ \_ \_ \_ EX**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**ID DI \_ PROTEZIONE \_ DELL'OUTPUT VIDEO \_ \_ DRM**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





