---
title: DRM_OUTPUT_PROTECTION struttura (Wmdrmsdk.h)
description: La struttura DRM \_ OUTPUT PROTECTION contiene informazioni su una tecnologia di protezione \_ dell'output.
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- DRM_OUTPUT_PROTECTION struttura windows Media Format
- Struttura windows Media Format
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82454d8b4982e6546b003ae3977c7a98869d46ba393ea49f0b97773f95572777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881131"
---
# <a name="drm_output_protection-structure"></a>Struttura DRM \_ OUTPUT \_ PROTECTION

La **struttura DRM \_ OUTPUT \_ PROTECTION** contiene informazioni su una tecnologia di protezione dell'output.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**guidId**
</dt> <dd>

GUID che identifica la tecnologia di protezione dell'output.

</dd> <dt>

**bConfigData**
</dt> <dd>

Dati di configurazione per la tecnologia.

</dd> </dl>

## <a name="remarks"></a>Commenti

**DRM \_ AUDIO \_ OUTPUT \_ PROTECTION** e **DRM VIDEO OUTPUT \_ \_ \_ PROTECTION** sono entrambi definiti **come DRM OUTPUT \_ \_ PROTECTION** nelle **istruzioni typedef.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PROTEZIONE \_ DELL'OUTPUT DRM \_ \_ EX**](drm-output-protection-ex.md)
</dt> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





