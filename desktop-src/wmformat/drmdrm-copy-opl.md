---
title: DRM_COPY_OPL struttura (Wmdrmsdk.h)
description: La struttura OPL DRM COPY contiene informazioni sui livelli di \_ protezione dell'output (OPL) specificati in una \_ licenza per le azioni di copia.
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- DRM_COPY_OPL struttura windows Media Format
- struttura windows Media Format
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
ms.openlocfilehash: d2ec6e376b2df4cd3e5462766d6fd992ed7d2356a1bc81d0ff74c662a99697af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708981"
---
# <a name="drm_copy_opl-structure"></a>Struttura \_ OPL COPY \_ DRM

La **struttura \_ \_ OPL DRM COPY** contiene informazioni sui livelli di protezione dell'output (OPL) specificati in una licenza per le azioni di copia.

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

[**DRM \_ Struttura OPL \_ OUTPUT \_ IDS**](drmdrm-opl-output-ids.md) contenente gli identificatori delle tecnologie da consentire. Questo membro viene usato per le tecnologie di output a cui vengono assegnati opl inferiori al livello di copia minimo, ma in cui è possibile copiare il contenuto.

</dd> <dt>

**oplIdExcludes**
</dt> <dd>

[**DRM \_ Struttura OPL \_ OUTPUT \_ IDS**](drmdrm-opl-output-ids.md) contenente gli identificatori di output delle tecnologie da limitare. Questo membro viene usato per le tecnologie di output a cui vengono assegnati file OPL che superano il livello di copia minimo, ma che l'emittente della licenza non concede i diritti per la copia.

</dd> </dl>

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

 

 





