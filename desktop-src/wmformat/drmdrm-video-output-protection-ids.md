---
title: Struttura DRM_VIDEO_OUTPUT_PROTECTION_IDS (wmdrmsdk. h)
description: La \_ \_ \_ struttura degli ID di protezione dell'output del video DRM \_ include una matrice di \_ strutture di protezione dell'output video DRM \_ \_ .
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- Formato di Windows Media per la struttura DRM_VIDEO_OUTPUT_PROTECTION_IDS
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51af3ccebec52ab6f6863aeb376ed27f8c8e2467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324450"
---
# <a name="drm_video_output_protection_ids-structure"></a>\_Struttura degli \_ ID di protezione dell'output del video DRM \_ \_

La struttura degli **ID di protezione dell' \_ output del video \_ \_ \_ DRM** include una matrice di strutture di **\_ \_ \_ protezione dell'output video DRM** .

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**Centri di**
</dt> <dd>

Numero di elementi nella matrice a cui fa riferimento **rgVop**.

</dd> <dt>

**rgVop**
</dt> <dd>

Indirizzo di una matrice di strutture di **\_ \_ \_ protezione dell'output video DRM** . **DRM \_ La \_ \_ protezione dell'output video** è un tipo definito come [**\_ \_ protezione dell'output DRM**](drm-output-protection.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata come membro della struttura [**DRM \_ Play \_ OPL**](drmdrm-play-opl.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ID di \_ protezione dell'output audio \_ DRM \_**](drm-audio-output-protection-ids.md)
</dt> <dt>

[**\_ \_ \_ ID protezione output video \_ DRM \_ es.**](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





