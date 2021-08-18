---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS struttura (Wmdrmsdk.h)
description: La struttura DRM \_ VIDEO \_ OUTPUT PROTECTION \_ \_ IDS contiene una matrice di strutture DRM \_ VIDEO OUTPUT \_ \_ PROTECTION.
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS struttura windows Media Format
- Struttura windows Media Format
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
ms.openlocfilehash: 9439328ed817da40630c3a600cf7e6db553738a12799babbe9e71c48f28923b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119085873"
---
# <a name="drm_video_output_protection_ids-structure"></a>Struttura DRM \_ VIDEO \_ OUTPUT PROTECTION \_ \_ IDS

La **struttura DRM \_ VIDEO OUTPUT \_ PROTECTION \_ \_ IDS** contiene una matrice **di strutture DRM VIDEO OUTPUT \_ \_ \_ PROTECTION.**

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**cEntries**
</dt> <dd>

Numero di elementi nella matrice a cui fa riferimento **rgVop**.

</dd> <dt>

**rgVop**
</dt> <dd>

Indirizzo di una matrice di **strutture DRM \_ VIDEO OUTPUT \_ \_ PROTECTION.** **DRM \_ VIDEO \_ OUTPUT \_ PROTECTION** è un tipo definito come [**DRM OUTPUT \_ \_ PROTECTION.**](drm-output-protection.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata come membro della struttura [**\_ \_ OPL DRM PLAY.**](drmdrm-play-opl.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID PROTEZIONE \_ OUTPUT AUDIO \_ \_ \_ DRM**](drm-audio-output-protection-ids.md)
</dt> <dt>

[**ID DI \_ PROTEZIONE DELL'OUTPUT VIDEO DRM \_ \_ \_ \_ EX**](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





