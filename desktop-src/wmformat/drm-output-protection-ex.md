---
title: Struttura DRM_OUTPUT_PROTECTION_EX (wmdrmsdk. h)
description: La \_ \_ struttura ex protezione dell'output DRM \_ include informazioni su una tecnologia di protezione dell'output. Questa struttura estende \_ \_ la protezione dell'output DRM aggiungendo un numero di versione.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- Formato di Windows Media per la struttura DRM_OUTPUT_PROTECTION_EX
- struttura Windows Media Format
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
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332661"
---
# <a name="drm_output_protection_ex-structure"></a>\_ \_ Struttura ex protezione dell'output DRM \_

La **struttura \_ \_ \_ ex protezione dell'output DRM** include informazioni su una tecnologia di protezione dell'output. Questa struttura estende **la \_ \_ protezione dell'output DRM** aggiungendo un numero di versione.

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

**DRM \_ La protezione output AUDIO \_ \_ \_ ex** e **DRM \_ video \_ \_ \_** , ad esempio, sono entrambi definiti come **\_ \_ protezione dell'output DRM** nelle istruzioni **typedef** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_protezione dell'output DRM \_**](drm-output-protection.md)
</dt> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





