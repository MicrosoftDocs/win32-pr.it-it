---
title: Struttura DRM_COPY_OPL (wmdrmsdk. h)
description: La \_ \_ struttura OPL copia DRM include informazioni sui livelli di protezione dell'output (OPLs) specificati in una licenza per le azioni di copia.
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- Formato di Windows Media per la struttura DRM_COPY_OPL
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_COPY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28655e220588bb704567de033e1117dd569d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330884"
---
# <a name="drm_copy_opl-structure"></a>\_ \_ Struttura OPL copia DRM

La **struttura \_ \_ OPL copia DRM** include informazioni sui livelli di protezione dell'output (OPLs) specificati in una licenza per le azioni di copia.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_COPY_OPL {
  WORD               wMinimumCopyLevel;
  DRM_OPL_OUTPUT_IDS oplIdIncludes;
  DRM_OPL_OUTPUT_IDS oplIdExcludes;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**wMinimumCopyLevel**
</dt> <dd>

OPL minimo per le azioni di copia.

</dd> <dt>

**oplIdIncludes**
</dt> <dd>

[**DRM \_ Struttura \_ di \_ ID output OPL**](drmdrm-opl-output-ids.md) contenente gli identificatori delle tecnologie da consentire. Questo membro viene utilizzato per le tecnologie di output a cui sono assegnati OPLs inferiori al livello di copia minimo, ma in cui è possibile copiare il contenuto.

</dd> <dt>

**oplIdExcludes**
</dt> <dd>

[**DRM \_ OPL \_ \_ ID output**](drmdrm-opl-output-ids.md) struttura contenente gli identificatori di output delle tecnologie da limitare. Questo membro viene utilizzato per le tecnologie di output a cui sono assegnati OPLs che superano il livello di copia minimo, ma che l'emittente della licenza non concede i diritti per la copia in.

</dd> </dl>

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

 

 





