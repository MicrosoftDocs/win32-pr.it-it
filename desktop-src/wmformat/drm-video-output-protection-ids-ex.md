---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX struttura (Wmdrmsdk.h)
description: La struttura DRM \_ VIDEO \_ OUTPUT PROTECTION \_ \_ IDS EX contiene una matrice di \_ strutture DRM VIDEO OUTPUT \_ \_ \_ PROTECTION.
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX struttura windows Media Format
- struttura windows Media Format
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5482734c2ded470b4e3dc885e32505c556b3106a12518969622f8007cf6e4f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704088"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a>Struttura DRM \_ VIDEO \_ OUTPUT PROTECTION \_ \_ IDS \_ EX

La **struttura DRM \_ VIDEO OUTPUT \_ PROTECTION \_ \_ IDS \_ EX** contiene una matrice di **strutture DRM VIDEO OUTPUT \_ \_ \_ PROTECTION.**

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

Numero di versione.

</dd> <dt>

**CEntries**
</dt> <dd>

Numero di elementi nella matrice a cui fa riferimento **rgVop.**

</dd> <dt>

**rgVop**
</dt> <dd>

Indirizzo di una matrice di **strutture \_ DRM VIDEO \_ OUTPUT PROTECTION \_ \_ EX.** **DRM \_ VIDEO \_ OUTPUT \_ PROTECTION \_ EX** è un tipo definito come [**PROTEZIONE OUTPUT DRM \_ \_ \_ EX**](drm-output-protection-ex.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID DI \_ PROTEZIONE \_ DELL'OUTPUT AUDIO \_ DRM, AD \_ \_ ESEMPIO**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**ID PROTEZIONE OUTPUT VIDEO DRM \_ \_ \_ \_**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





