---
title: Struttura DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX (wmdrmsdk. h)
description: La \_ \_ \_ \_ struttura ad esempio ID protezione output audio DRM \_ contiene un elenco di identificatori di protezione dell'output audio. Questa struttura estende gli \_ \_ \_ ID protezione dell'output audio DRM \_ aggiungendo un numero di versione.
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- Formato di Windows Media per la struttura DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb687b5600e75f845c2d980f73f3b8c2eeda970a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332288"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a>\_ \_ ID protezione output audio DRM- \_ \_ \_ struttura ex

La struttura ad **\_ \_ \_ \_ \_ esempio ID protezione output audio DRM** contiene un elenco di identificatori di protezione dell'output audio. Questa struttura estende **gli \_ \_ \_ \_ ID protezione dell'output audio DRM** aggiungendo un numero di versione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION_EX *rgAop;
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

Numero di voci nella matrice **rgAop** .

</dd> <dt>

**rgAop**
</dt> <dd>

Matrice di **strutture \_ \_ \_ \_ ex protezione output audio DRM** . **DRM \_ La \_ Protezione output audio \_ \_ ex** è un tipo definito [**come \_ protezione dell'output \_ \_ DRM**](drm-output-protection-ex.md), ad esempio.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna.

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

 

 





