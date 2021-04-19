---
title: Struttura DRM_OPL_OUTPUT_IDS (wmdrmsdk. h)
description: La \_ struttura degli \_ \_ ID di output di DRM OPL include un numero di identificatori di output OPL (output Protection Level).
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- Formato di Windows Media per la struttura DRM_OPL_OUTPUT_IDS
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802787c5e373c837d639e0225bf650d80c105970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330249"
---
# <a name="drm_opl_output_ids-structure"></a>\_Struttura di \_ ID output OPL \_ DRM

La struttura degli **\_ ID di \_ output \_ di DRM OPL** include un numero di identificatori di output OPL (output Protection Level).

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**CID**
</dt> <dd>

Numero di identificatori nella matrice a cui fa riferimento **rgIds**.

</dd> <dt>

**rgIds**
</dt> <dd>

Indirizzo di una matrice di GUID. Ogni membro della matrice contiene un identificatore di output OPL.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata come membro delle strutture di [**\_ copia DRM \_ OPL**](drmdrm-copy-opl.md) e [**DRM \_ Play \_ OPL**](drmdrm-play-opl.md) per identificare i gruppi di identificatori di output.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





