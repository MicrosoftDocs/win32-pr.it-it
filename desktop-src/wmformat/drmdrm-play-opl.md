---
title: DRM_PLAY_OPL struttura (Wmdrmsdk.h)
description: La struttura OPL DRM PLAY contiene informazioni sui livelli di protezione \_ \_ dell'output specificati in una licenza per le azioni di riproduzione.
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- DRM_PLAY_OPL struttura windows Media Format
- Struttura windows Media Format
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f649263db5435310d076386c49b2e77960552646e7ea2325190c3f0b94f27bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708311"
---
# <a name="drm_play_opl-structure"></a>Struttura OPL DRM \_ PLAY \_

La **struttura \_ \_ OPL DRM PLAY** contiene informazioni sui livelli di protezione dell'output specificati in una licenza per le azioni di riproduzione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**minOPL**
</dt> <dd>

[**DRM \_ Struttura MINIMUM \_ OUTPUT \_ PROTECTION \_ LEVELS**](drmdrm-minimum-output-protection-levels.md) contenente l'OPL minimo necessario per riprodurre il contenuto in formati diversi.

</dd> <dt>

**oplIdReserved**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> <dt>

**vopi**
</dt> <dd>

[**DRM \_ Struttura \_ VIDEO OUTPUT PROTECTION \_ \_ IDS**](drmdrm-video-output-protection-ids.md) contenente gli identificatori di protezione dell'output video applicabili alla riproduzione del contenuto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DRM \_ COPY \_ OPL**](drmdrm-copy-opl.md)
</dt> <dt>

[**DRM \_ PLAY \_ OPL \_ EX**](drm-play-opl-ex.md)
</dt> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





