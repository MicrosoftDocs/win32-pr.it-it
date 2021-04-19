---
title: Struttura DRM_PLAY_OPL (wmdrmsdk. h)
description: La \_ struttura OPL di riproduzione DRM \_ include informazioni sui livelli di protezione dell'output (OPLs) specificati in una licenza per le azioni di riproduzione.
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- Formato di Windows Media per la struttura DRM_PLAY_OPL
- struttura Windows Media Format
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
ms.openlocfilehash: 8a40d8fe4e8b3c820f9d7bcb405b5c0806040182
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333625"
---
# <a name="drm_play_opl-structure"></a>\_Struttura OPL della riproduzione DRM \_

La **struttura \_ \_ OPL di riproduzione DRM** include informazioni sui livelli di protezione dell'output (OPLs) specificati in una licenza per le azioni di riproduzione.

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

[**DRM \_ Struttura \_ dei \_ \_ livelli di protezione dell'output minima**](drmdrm-minimum-output-protection-levels.md) che contiene il OPL minimo richiesto per riprodurre contenuto in formati diversi.

</dd> <dt>

**oplIdReserved**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> <dt>

**vopi**
</dt> <dd>

[**DRM \_ Struttura \_ degli \_ \_ ID di protezione dell'output video**](drmdrm-video-output-protection-ids.md) contenente gli identificatori di protezione dell'output video che si applicano alla riproduzione del contenuto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_copia DRM \_ OPL**](drmdrm-copy-opl.md)
</dt> <dt>

[**DRM \_ Play \_ OPL \_ ex**](drm-play-opl-ex.md)
</dt> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





