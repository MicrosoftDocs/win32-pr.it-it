---
title: DRM_OPL_OUTPUT_IDS struttura (Wmdrmsdk.h)
description: La struttura \_ DRM OPL OUTPUT IDS contiene una serie di identificatori di \_ output \_ OPL (Output Protection Level).
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- DRM_OPL_OUTPUT_IDS struttura windows Media Format
- struttura windows Media Format
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
ms.openlocfilehash: 265e1015dd31281043d388debc802b390e7dd2d534f426ecbe24402efffd13df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658861"
---
# <a name="drm_opl_output_ids-structure"></a>Struttura DRM \_ OPL \_ OUTPUT \_ IDS

La **struttura \_ DRM OPL \_ OUTPUT \_ IDS** contiene una serie di identificatori di output OPL (Output Protection Level).

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**cIds**
</dt> <dd>

Numero di identificatori nella matrice a cui fa riferimento **rgIds**.

</dd> <dt>

**rgIds**
</dt> <dd>

Indirizzo di una matrice di GUID. Ogni membro della matrice contiene un identificatore di output OPL.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata come membro delle strutture [**\_ \_ OPL DRM COPY**](drmdrm-copy-opl.md) e [**DRM PLAY \_ \_ per**](drmdrm-play-opl.md) identificare i gruppi di identificatori di output.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





