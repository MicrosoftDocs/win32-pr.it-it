---
title: DRM_PLAY_OPL_EX struttura (Wmdrmsdk.h)
description: La struttura DRM PLAY OPL EX contiene informazioni sui livelli di protezione \_ \_ \_ dell'output specificati in una licenza per le azioni di riproduzione.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- DRM_PLAY_OPL_EX struttura windows Media Format
- Struttura windows Media Format
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89ca0c6b1cf33a422265fb177e1b1432a52fbd12b3f9fda658125682f3888ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848440"
---
# <a name="drm_play_opl_ex-structure"></a>Struttura DRM \_ PLAY \_ OPL \_ EX

La **struttura DRM \_ PLAY \_ OPL \_ EX** contiene informazioni sui livelli di protezione dell'output specificati in una licenza per le azioni di riproduzione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

Numero di versione.

</dd> <dt>

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

## <a name="remarks"></a>Commenti

Questa struttura è identica alla struttura **\_ \_ OPL DRM PLAY,** ad eccezione del fatto che include un numero di versione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md)
</dt> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





