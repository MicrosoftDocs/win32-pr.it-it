---
title: DRM_OUTPUT_PROTECTION_EX struttura (Wmdrmsdk.h)
description: La struttura DRM \_ OUTPUT PROTECTION EX contiene informazioni su una tecnologia di protezione \_ \_ dell'output. Questa struttura estende DRM \_ OUTPUT PROTECTION aggiungendo un numero di \_ versione.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- DRM_OUTPUT_PROTECTION_EX struttura windows Media Format
- struttura windows Media Format
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac3033482dc84ad8a25e2e18c359cd621228fef37cc97673f9a5eeae9a57b1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029585"
---
# <a name="drm_output_protection_ex-structure"></a>Struttura DRM \_ OUTPUT \_ PROTECTION \_ EX

La **struttura DRM \_ OUTPUT PROTECTION \_ \_ EX** contiene informazioni su una tecnologia di protezione dell'output. Questa struttura estende **DRM \_ OUTPUT \_ PROTECTION** aggiungendo un numero di versione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

Numero di versione.

</dd> <dt>

**guidId**
</dt> <dd>

GUID che identifica la tecnologia di protezione dell'output.

</dd> <dt>

**dwConfigData**
</dt> <dd>

Dati di configurazione per la tecnologia.

</dd> </dl>

## <a name="remarks"></a>Commenti

**DRM \_ AUDIO \_ OUTPUT \_ PROTECTION \_ EX** e **DRM VIDEO OUTPUT PROTECTION \_ \_ \_ \_ EX** sono entrambi definiti come **PROTEZIONE OUTPUT DRM \_ \_** nelle **istruzioni typedef.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PROTEZIONE \_ DELL'OUTPUT \_ DRM**](drm-output-protection.md)
</dt> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





