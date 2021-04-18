---
title: Struttura DRM_PLAY_OPL_EX (wmdrmsdk. h)
description: La \_ struttura ex di DRM Play \_ OPL \_ include informazioni sui livelli di protezione dell'output (OPLs) specificati in una licenza per le azioni di riproduzione.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- Formato di Windows Media per la struttura DRM_PLAY_OPL_EX
- struttura Windows Media Format
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
ms.openlocfilehash: edf85ee664b33df9c63c390a870401b100327f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329052"
---
# <a name="drm_play_opl_ex-structure"></a>\_ \_ Struttura ex OPL di DRM Play \_

La struttura **ex di DRM \_ Play \_ OPL \_** include informazioni sui livelli di protezione dell'output (OPLs) specificati in una licenza per le azioni di riproduzione.

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

## <a name="remarks"></a>Commenti

Questa struttura è identica alla struttura **\_ \_ OPL di riproduzione DRM** , ad eccezione del fatto che include un numero di versione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_riproduzione DRM \_ OPL**](drmdrm-play-opl.md)
</dt> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





