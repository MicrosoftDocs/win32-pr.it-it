---
title: Struttura DRM_OUTPUT_PROTECTION (wmdrmsdk. h)
description: La \_ \_ struttura di protezione dell'output DRM include informazioni su una tecnologia di protezione dell'output.
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- Formato di Windows Media per la struttura DRM_OUTPUT_PROTECTION
- struttura Windows Media Format
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
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329055"
---
# <a name="drm_output_protection-structure"></a>Struttura di protezione dell' \_ output DRM \_

La struttura di **\_ \_ protezione dell'output DRM** include informazioni su una tecnologia di protezione dell'output.

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

**DRM \_ La \_ \_** protezione dell'output audio e la **\_ \_ \_ protezione dell'output video DRM** sono entrambe definite come **\_ \_ protezione dell'output DRM** nelle istruzioni **typedef** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**protezione dell'output DRM, ad \_ \_ \_ esempio**](drm-output-protection-ex.md)
</dt> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





