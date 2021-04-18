---
title: Struttura DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX (wmdrmsdk. h)
description: La \_ \_ \_ \_ struttura ad esempio ID protezione output video DRM \_ include una matrice di \_ strutture di protezione dell'output video DRM \_ \_ .
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- Formato di Windows Media per la struttura DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
- struttura Windows Media Format
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
ms.openlocfilehash: a2e7cc5ec0b4b14d88deb317e62e3e1cd4f92b57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324049"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a>\_ \_ ID protezione output video DRM- \_ \_ \_ struttura ex

La struttura ad **\_ \_ \_ \_ \_ esempio ID protezione output video DRM** include una matrice di strutture di **\_ \_ \_ protezione dell'output video DRM** .

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

**Centri di**
</dt> <dd>

Numero di elementi nella matrice a cui fa riferimento **rgVop**.

</dd> <dt>

**rgVop**
</dt> <dd>

Indirizzo di una matrice di **strutture \_ \_ \_ \_ ex protezione output video DRM** . **DRM \_ La \_ protezione dell'output \_ \_ video** è un tipo definito [**come \_ \_ protezione dell' \_ output DRM**](drm-output-protection-ex.md), ad esempio.

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

 

 





